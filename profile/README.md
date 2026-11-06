# Aether Poem · 白噪诗

A research and creative team working on one question: what does it take for a
literary text to become an interactive world that can actually be run, and
checked?

We work across literary and language research, game design, and software
engineering. Research, playable worlds, the systems that run them, and public
testing are four forms of the same work; each is meant to answer to the others.

Contact: yuanyuhao2004@outlook.com

## What we work on

- **Research** — literary reading, AI imitation and authorship, platform
  narrative, and digital humanities questions, each reported with its material,
  method, and status.
- **Worlds** — literary material (Joyce's *The Dead*, among others) organised
  into characters, relationships, information, places, and choices that can be
  played.
- **Systems** — the toolchain that designs a module, runs it as an authoritative
  session, and connects it to a group chat.
- **In public** — playtests, conference presentations, and demos, where the
  method meets participants and peers.

TRPG is one field where we test this way of working, not the only medium we work
in.

## How the toolchain fits together

```text
literary text / design basis
        │
        ▼
  Narrative Forge        design workspace: basis → world frame → module spec
        │
        ▼
  module.spec.v3         shared contract (aether-poem-contracts)
        │
        ▼
  Backend Core           authoritative session: roll resolution, state,
        │                committed event history
        ▼
  QQ bot (group play) / browser client
```

Three rules hold across the whole chain:

- AI proposes, rules adjudicate, the session commits. A language model never
  writes world state directly.
- Every state change is an immutable event appended to history. Corrections are
  new events that reference the corrected one.
- Every random draw carries an explicit seed, so a table can be replayed.

## Repositories

| Repository | What it is |
| --- | --- |
| [trpg-world-status](https://github.com/aether-poem/trpg-world-status) | The earlier world-state pipeline: narrative text → structured characters, places, relationships, quests, and story state. Predecessor of the current design. |
| [multi-perspective-module](https://github.com/aether-poem/multi-perspective-module) | A playable TRPG investigation and emotional-interaction minitest. |
| [literary-empathy-prototype](https://github.com/aether-poem/literary-empathy-prototype) | Archived early prototype on multi-perspective storytelling. |

The runtime toolchain — Narrative Forge, Backend Core, the shared module
contracts, and the QQ bot adapter — is in active development and its
repositories are currently private. Test instances are opened by invitation;
there is no public self-service deployment yet.

## Current status

- A literary TRPG adaptation of Joyce's *The Dead* was presented at CDH 2026.
- The toolchain is under development; interfaces are still moving.

## Team

Aether Poem was started by students at the College of Foreign Languages, Nankai
University, and works with collaborators in narrative design and software
engineering. Project lead: Yuan Yuhao (袁禹豪).

于喧嚣白噪中执笔成诗。
