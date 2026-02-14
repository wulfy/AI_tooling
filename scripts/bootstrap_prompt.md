Create an IDE-agnostic `.agents/` directory for this project.

Inputs:
- Specify project language

Deliverables:
1) Propose `.agents/` folder structure (prompts/, rules/, skills/, agents/, config/).
2) Generate:
   - prompts/system.md (short)
   - rules/00-foundations.md
   - rules/05-environment-docker.md (if docker is configured in project)
   - rules/15-architecture.md
   - rules/17-bounded-context.md
3) Generate agents/backend.yaml and agents/architect.yaml that include the right rules/skills in deterministic order.
Keep files concise and avoid duplication (system.md should not contain detailed directory trees).