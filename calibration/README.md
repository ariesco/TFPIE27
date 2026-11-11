# Calibration model: publish-subscribe

`pubsub.maude` is the model we wrote before setting the assignment, to see
what a team's work would actually look like. It is published as an example
of a specification that would **not** earn top marks under the rubric, and
of why.

It is unfinished and is published as it was, including the `TODO` before
`eof` and the notes after it. Only the comments and those notes have been
translated from Spanish; the code is untouched.

## What it does

The model follows Google Cloud Pub/Sub. Four classes: publishers, topics,
subscriptions (a map from subscriber to message filter), and subscribers,
which accumulate what they receive. Messages are JSON values.

The equational layer does the routing. The two `broadcast` functions are
structural recursion over a list of subscriptions and over a map of
subscribers, the second guarded by the filter:

```maude
op broadcast : Map{SubscriberId, Filter} JSON -> Configuration .
eq broadcast(empty, J) = none .
eq broadcast((SID |-> F, MSF), J) = if evalAttributes(J, F)
                                    then to SID : J
                                    else none
                                    fi
                                    broadcast(MSF, J) .
```

The rule layer has four rules: publisher to topic, topic to subscription,
subscription to its matching subscribers, subscriber accumulates.

## Why it would not earn top marks

The signature mirrors the real system closely: publishers with an ordering
key and a retry policy, topics with a retention duration and a storage policy.
The notes after `eof` show where it came from: they are the attribute tables
of the Pub/Sub documentation, transcribed. It looks substantial.

But the four rules are unconditional and none of them can fail. There is no
acknowledgement and no redelivery, and the retry policy and the ordering key
are declared and never read by any rule. The properties a team would
naturally state, such as every published message reaching every matching
subscriber, hold by construction: the model checker confirms them without
the model ever having been at risk of violating them.

The heuristic we took from it is the one the menu is ordered by:
**difficulty lives in the rules, not in the signature.** A rich signature is
cheap; it can be transcribed from an API reference, with or without an
assistant. What separates a demanding model from a decorative one is how many
rules are conditional, what the model allows to go wrong, and whether any
stated property could actually fail. The `TODO` names what would have made
this one demanding: acknowledgements that can fail, and a retry policy with a
timeout and a maximum number of attempts.

## Loading it

The first line is `load ../json/json.maude`. Maude resolves that path
relative to `pubsub.maude`, so the JSON module has to be at `json/json.maude`
in the root of this repository. Then:

```
maude calibration/pubsub.maude
```

## Why publish-subscribe is not on the menu

A team that chose publish-subscribe would have this model in front of them,
so the system was taken off the menu. In a modeling course, every worked
model you publish retires a system.
