Digital Learning Companion (DLC)

Deterministic AI for Writing & Learning.

The Digital Learning Companion (DLC) is an open-core, turn-based educational system built on the Emergent State Machine (ESM) architecture.

It is designed to make AI-driven learning:

Auditable

Deterministic

Policy-governed

Replayable

Transparent to teachers and students

What Is the DLC?

The DLC is a structured learning engine that:

Interprets student input deterministically

Produces versioned telemetry

Tracks learning signals over time

Surfaces focus components (e.g., writing structure)

Calculates volatility windows

Generates deterministic assistant guidance (no black-box drift)

This is not a chat toy.

It is a controlled mutation system for education.

Architecture Overview

The DLC is built from two primary components:

1️⃣ dlc_brain (FastAPI)

Deterministic turn engine.

/turn endpoint

Domain analyzers (e.g., writing.structure)

Telemetry generation

Volatility tracking

Structured student model deltas

2️⃣ dlc_web (Phoenix LiveView)

Public demo interface.

Writing Tutor LiveView

Deterministic assistant messaging

Telemetry visualization

Focus + support tier tracking

Assessment panel (optional)

All state mutation happens through explicit, versioned updates.

Core Principle

Behavioral change must occur through explicit, versioned policy mutation — never through implicit LLM drift.

The DLC uses the Emergent State Machine (ESM) pattern to separate:

Descriptive state

Deterministic authority

Optional generative instrumentation

Repositories

🧠 dlc_brain — Deterministic turn engine

🌐 dlc_web — Phoenix LiveView demo

📐 esm-spec — Normative specification of the Emergent State Machine

🧱 Controlled Mutation Layer — Architectural framework

Why This Exists

Modern AI systems entangle:

Interpretation

Decision authority

Generative output

This makes them:

Difficult to audit

Impossible to replay deterministically

Unsafe for policy-sensitive domains

The DLC demonstrates a different path.

Current MVP

Writing Tutor demo includes:

Focus detection (position/support/link/context)

Issue codes (e.g., position_vague)

Deterministic assistant messages

Volatility window tracking

Structured telemetry output

No LLM required.

Open Core Philosophy

This project is:

Open for inspection

Open for research

Open for contribution

The specification (ESM) defines the pattern.
Implementations can evolve.

Getting Started (Local Dev)

See individual repo READMEs for setup instructions.

Typical development flow:

# brain

cd dlc_brain
PYTHONPATH=. python -m uvicorn dlc.app:app --port 8000

# web

cd dlc_web
mix phx.server
Audience

This project is for:

Learning scientists

Education technologists

Engineers building structured AI systems

Organizations requiring auditability

Status

Active development.
MVP writing tutor operational.
Control architecture stable.

Contact

Questions, architecture discussions, or collaboration inquiries are welcome.
