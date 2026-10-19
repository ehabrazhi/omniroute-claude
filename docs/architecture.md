# Architecture

This starter is intentionally independent of a language, framework, and model
provider. Select those choices before implementing the modules or setting up CI.

## Core areas

- **Agents** define task-specific behavior and lifecycle.
- **Runtime** executes agent turns and provides shared services.
- **Orchestration** coordinates tasks, handoffs, and multi-agent workflows.
- **Tools** expose typed, permission-checked capabilities to agents.
- **Memory** owns persistence, retrieval, and retention boundaries.
- **Policies** centralize authorization, safety, and governance rules.
- **Interfaces** connect users and external systems to the runtime.

Keep provider-specific integrations behind interfaces so they can be replaced
without changing orchestration or agent behavior.

## Security boundaries

- Treat model output, tool arguments, retrieved content, and external input as
  untrusted.
- Enforce authorization in the runtime or tool implementation, not only in
  prompts.
- Keep credentials outside the repository and avoid logging secret values.
- Define retention and access rules before persisting conversation or memory
  data.

## Decisions to make

Record the selected language, runtime, model/provider interface, persistence
strategy, deployment target, and test approach here as the project takes shape.
