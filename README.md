## James Munluah

I build and operate production systems with coding agents, and I keep the
receipts on what actually works.

For about two years I have run a four-line operations platform for a small
business group in India - laundry, courier, a diner, property - as a single
developer working with an agent as the primary implementer. Real money moves
through it daily. Roughly 181,000 lines of TypeScript, 274 database migrations,
560 test files, ~2,600 commits.

The thing that made it survivable was not prompt engineering. It was learning
that **an agent's instructions are a hint, and only a mechanism is a mechanism.**

### [agent-operating-system](https://github.com/james-munluah/agent-operating-system)

The mechanisms, extracted and generalised from that private system.

- **Hooks that fail closed** - refuse a tool call that would read a real `.env`;
  refuse a destructive git command *only* when the tree is dirty, and name what
  would be lost.
- **A Stop hook that audits the agent's own claims** - blocks the turn when a
  cause, coverage or capability is asserted with no check attached.
- **Eight review lenses** that fire by risk class, plus a runner that makes them
  executable against any diff with typed findings and a gate exit code.
- **A confidentiality gate whose denylist cannot leak its own terms.** Its first
  draft failed its own scan on eleven lines, because a denylist written in
  plaintext *is* the leak.

The README carries a table of what is proven and what is not, including the
rows that are uncomfortable. That habit is the point of the repository.

### What I am interested in

Agent harness design: guardrails, evals, routing, and the unglamorous question
of how you know an agent-built system is actually correct. I care more about the
check that catches the defect than the patch that fixes it.

### Elsewhere

Most of my work is client code and stays private. If you want depth on something
specific, ask - I can usually talk through the design without shipping the source.
