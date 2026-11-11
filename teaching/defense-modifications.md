# The defense

Each team defends its project in person: 20 minutes for a pair, 25 for a
trio. Each member is questioned about their own part of the work and is asked
for one small modification to the team's specification. Students know a
modification will be asked for, but not which one.

## What to ask

Twenty minutes is not enough to go through the whole project, so the
questions go to what cannot be improvised:

- a specific modeling decision and why it was taken that way
  (*why is this an equation and not a rule?*);
- what the verified property does and does not guarantee;
- what real failure one of the team's mutations represents.

## The live modification

This is the part that cannot be delegated, so it is the backbone of the
defense. One per member, small, specific to the team's project. A repertoire
that works with almost any system on the menu:

| Ask | What it checks |
|---|---|
| Add one more agent, node, or client to the example term. What happens to the state space? | That they understand the configuration and where the combinatorial growth comes from. |
| Relax this guard. Which property breaks, and what is the shortest counterexample? | That they know which condition each property rests on. |
| Turn this rule into an equation. Is the model still correct? What does the model checker gain? | Part 6 of the statement, which a report can answer by rote. |
| Propose a mutation different from the two you submitted, one that breaks the *other* property. | That the mutations were theirs. |
| Change the example term so that the property fails. | That they distinguish the model from the particular instance they verified. |

## Prediction first, then execution

Ask for the prediction *before* running Maude: that is where understanding
shows. Running it only confirms. This also protects the student who reasons
well but stumbles over syntax: a typing slip should not count the same as a
wrong prediction.

## Two practical points

- Ask teams to come with their code already loaded. A model that takes two
  minutes to start uses up a tenth of the slot.
- Prepare each team's modification in advance, from its report, over the
  weekend between submission and the first defense. Improvising it on the
  spot is the quickest way to ask for something that cannot be done in three
  minutes.
