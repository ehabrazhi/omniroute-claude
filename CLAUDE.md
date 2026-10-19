# Project instructions

- Keep the implementation modular across agents, runtime, orchestration, tools,
  memory, policies, and interfaces.
- Do not commit credentials, access tokens, private keys, or populated local
  environment files.
- Define and test explicit permissions at tool boundaries; do not give an agent
  broader access than its task requires.
- Record architectural decisions in `docs/architecture.md`.
- Once a language and runtime are selected, document the setup and test commands
  here and add matching automated checks.
