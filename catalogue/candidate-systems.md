# Candidate systems

The twelve systems offered to teams in 2026/27, in the order they appear in
the project statement: from the most to the least demanding. Teams may also
propose a system of their own, subject to the instructor's approval.

Each entry is tagged with the team size its scope is meant for: **[3]** calls
for a trio, **[2]** fits a pair, **[2–3]** works with either, and **[3–4]**
also admits a group of four. A group that takes a system scoped for a smaller
team gets additional requirements; the two cases of 2026/27 are below. The tag is a
recommendation, not a restriction. Depth of development is judged relative to
team size, so choosing a system tagged [2] does not cap the grade.

| # | System | Properties it invites | Team |
|---|---|---|---|
| 1 | Simplified Raft-style consensus (leader election plus log replication) | At most one leader per term; committed entries are not lost when a minority of nodes fail | [3–4] |
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

### Raft for a group of four

In 2026/27 one team of four took Raft. A group of four must, in addition:

- allow a node to crash and recover at any time, keeping only its persistent
  state (current term, vote cast, and log), and the network to lose messages;
- state and verify *Log Matching* (if two logs contain an entry with the same
  index and term, they are identical up to that index) and *Leader
  Completeness* (every leader contains all entries committed in earlier
  terms);
- include, among its mutations, one that removes the election restriction (a
  node votes only for candidates whose log is at least as up to date as its
  own), with a Maude counterexample in which a committed entry is lost;
- justify the bounds used (number of nodes, of terms, and log length) and
  report how many states each check explores.

The extension deepens what the team models instead of enlarging the system:
Raft's state space is already the binding constraint in four weeks. The
election restriction is the part of Raft that is least understood from
reading the paper and best understood by breaking it, and its counterexample
needs only three nodes and two terms.

### Producer-consumer for a group of three

In 2026/27 one team of three took producer-consumer, which is scoped for
pairs. A group of three must, in addition:

- model at least two producers and two consumers, and represent the
  synchronization mechanism explicitly (a monitor with condition variables,
  or semaphores), with processes that block and are woken up, instead of
  relying only on guards in the rules;
- state and verify absence of deadlock, FIFO order of each producer's
  messages, and absence of starvation of any process, the last one in LTL
  under a fairness assumption expressed in the formula itself and justified
  in the report;
- include, among its mutations, one that reproduces the *lost wake-up*: a
  monitor with a single condition variable that wakes one process instead of
  all of them, with a Maude counterexample in which every process is waiting;
- justify the bounds used (number of processes and buffer size) and report
  how many states each check explores.

As with Raft, the extension deepens the model instead of changing the
system. The lost wake-up is the classic bug of this problem, and it only
appears with more than one producer and more than one consumer, which is why
the extension asks for both.

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
