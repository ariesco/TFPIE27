# Candidate systems

The twelve systems offered to teams in 2026/27, in the order they appear in
the project statement: from the most to the least demanding. Teams may also
propose a system of their own, subject to the instructor's approval.

Each entry is tagged with the team size its scope is meant for: **[3]** calls
for a trio, **[2]** fits a pair, **[2–3]** works with either. The tag is a
recommendation, not a restriction. Depth of development is judged relative to
team size, so choosing a system tagged [2] does not cap the grade.

| # | System | Properties it invites | Team |
|---|---|---|---|
| 1 | Simplified Raft-style consensus (leader election plus log replication) | At most one leader per term; committed entries are not lost when a minority of nodes fail | [3] |
| 2 | Two-phase commit (2PC) | All participants decide the same outcome (atomicity); no indefinite blocking if the coordinator fails after the prepare phase | [3] |
| 3 | Distributed lock manager | Mutual exclusion between clients; no deadlock; the lock is released after its holder fails | [3] |
| 4 | Messaging system with delivery guarantees (at-least-once or exactly-once) | Every sent message is delivered at least once; no duplicates when exact delivery is required | [3] |
| 5 | Cache with invalidation (write-through or write-back) | Consistency between cache and persistent storage; no stale reads after an invalidation | [2–3] |
| 6 | Handshake of a real protocol (TCP three-way handshake, or a simplified TLS) | The handshake always ends in a consistent state on both ends | [2–3] |
| 7 | Leader election (bully algorithm or similar) | A single leader is elected, and it is always the highest-priority live node | [2–3] |
| 8 | Gossip protocol | Information eventually reaches all live nodes; state convergence | [2–3] |
| 9 | Producer-consumer with a bounded queue | No message loss; no buffer overflow; no consumer starvation | [2] |
| 10 | Rate limiter (token bucket or leaky bucket) | Never more requests than the configured limit in a time window; recovery after a traffic spike | [2] |
| 11 | Circuit breaker | The circuit opens after N consecutive failures; no calls to the failed service while it is open | [2] |
| 12 | Load balancer (round robin or least connections) | Fair distribution among active nodes; no failed node receives traffic | [2] |

## How the order was decided

The demanding entries are the ones whose headline property is only
interesting if the model admits failure. In a failure-free model of two-phase
commit, "no participant blocks if the coordinator fails" holds trivially,
because the coordinator never fails; the model checker confirms the property
in seconds and the model has proved nothing. The heuristic behind the order
is the one in [`calibration/`](../calibration/README.md): difficulty lives in
the rules, not in the signature.

| Group | System | Why it sits where it does |
|---|---|---|
| [3] | Raft-style consensus | Leader election plus log replication, terms and majorities. By far the largest entry. |
| | Two-phase commit | The blocking property forces the team to model coordinator failure; it cannot be avoided. |
| | Distributed lock manager | Releasing the lock after its holder fails is the core of the property, so failure and mutual exclusion must be modeled together. |
| | Messaging with guarantees | Exactly-once requires modeling duplication and loss; without them there is nothing to prove. |
| [2–3] | Cache with invalidation | Stale reads are a real property, but the model can be simplified a great deal. |
| | Protocol handshake | TCP's three-way handshake is small; a simplified TLS gives more. |
| | Leader election | Failures matter, but it is much smaller than Raft. |
| | Gossip | Convergence is rich, but the model can stay very simple. |
| [2] | Producer-consumer | Sound, but a textbook example with solutions everywhere. |
| | Rate limiter | A counter with a time window; little concurrency. |
| | Circuit breaker | A state machine with a counter. |
| | Load balancer | Round robin is a cursor: little can go wrong. |

A team that picks one of the [2] entries should be asked from the start
which failure mode it will model, since without one the project risks being
trivial.

## Not on the menu

Publish-subscribe was on the original list. It was withdrawn because the
calibration model published in [`calibration/`](../calibration/README.md) is a
publish-subscribe model, and a team choosing that system would have it in
front of them.
