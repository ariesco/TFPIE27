# Teaching plan

How the Maude block of *Auditoría, Calidad y Fiabilidad Informáticas* (UCM,
master's level) was organized in 2026/27, the first year of the project-based
assessment. Dates are those of that year.

## Context

- 16 students, in teams of two or three: six to eight teams.
- Eight weeks, two 100-minute sessions a week: a lecture on Monday and a
  laboratory session on Thursday.
- Three short practicals, one per Thursday in the first three weeks. They are
  handed in but carry no marks; the project carries the whole grade of the
  block (2.5 of the 10 points of the course).
- Teams form only once the practicals are over.

## Week by week

The statements of the three practicals are in [`practicals/`](../practicals/).


| Week | Dates | Lecture (Monday) | Laboratory (Thursday) |
|---|---|---|---|
| 1 | 26 and 29 Oct | Maude basics: functional modules, sorts, operators, equations | Practical 1 (ungraded): binary search tree |
| 2 | 2 and 5 Nov | **Project kickoff**: statement and menu of candidate systems, so that students think about a choice while doing the practicals. System modules and rewrite rules | Practical 2 (ungraded): modify the rules of a given specification, not write them from scratch |
| 3 | 9 and 12 Nov | `search` and state-space exploration | Practical 3 (ungraded): triangular peg solitaire solved with `search` |
| 4 | 16 and 19 Nov | **Monday: deadline** to form teams and choose a system, subject to approval. LTL and the model checker | Project work begins: sorts, operators, first equations and rules |
| 5 | 23 and 26 Nov | Worked examples: a ring protocol and a peer-to-peer protocol | Project work: base specification and the properties (part 3) |
| 6 | 30 Nov and 3 Dec | Equational abstraction: when a rule can become an equation, and what that does to the state space | Project work: verification with `search` and the LTL model checker |
| 7 | 7 and 10 Dec | Semantics of programming languages | Last working session: mutations (part 5), re-verification, report. **Submission: Friday 11, 23:59** |
| 8 | 14 and 17 Dec | **Defenses**, first round | **Defenses**, second round. End-of-term survey |

## Supervision without milestones

There are no graded intermediate deliverables. From week 4 every laboratory
session is a working session in which teams build their model in the room and
the instructor goes from desk to desk. A short note per team after each
session is enough to catch, while it is still cheap to fix:

- a model drifting towards the failure-free case (for instance, one that
  assumes communication never fails);
- a signature that keeps growing while the rules stay unconditional;
- a team in which one person is writing everything.

## Submission before the defenses

Submission is on the Friday before the defense week, not on the last day.
If teams defending on Thursday could submit after those defending on Monday,
they would have had three more days of project. It also leaves the weekend to
read the reports and prepare each team's questions.

## Defense logistics

At 20 minutes for a pair and 25 for a trio, the planned seven teams (two
trios and five pairs) need 150 minutes, which does not fit in one 100-minute session. Split
across the two sessions of the last week:

| Session | Teams | Time | |
|---|---|---|---|
| Monday 14 Dec | 3 pairs + 1 trio | 85 min | 15 min margin |
| Thursday 17 Dec | 2 pairs + 1 trio | 65 min | 35 min left for the survey |
| | | **150 min** | |

With eight pairs instead, the total is 160 minutes and still fits.

While one team defends, the rest work on the course's final presentation,
which is what that week is for. It is better to hold the defense away from
the room, so that a team does not hear the questions put to the previous one.

Because the contribution weighting comes from the task split declared in the
report, the defense does not have to reconstruct who did what: it only has to
check that each member understands what they submitted.

## Assigning systems to teams

The rubric rewards depth relative to team size, so trios are steered towards
the entries tagged [3]: with a rate limiter, a trio will find it hard to show
that depth. See [`catalogue/candidate-systems.md`](../catalogue/candidate-systems.md)
for the order and the reasoning. The choice remains the students'; the point
is to know what to propose instead when a trio arrives with a [2] system, and
to ask a team with a [2] system from the start which failure mode it will
model.

## End-of-term survey

Anonymous, voluntary, and carries no marks. It is handed out on paper in the
last 10 to 15 minutes of the final session, after the defenses, which is what
keeps the response rate up. On paper the anonymity is visible and does not
have to be taken on trust. See [`survey/`](../survey/).
