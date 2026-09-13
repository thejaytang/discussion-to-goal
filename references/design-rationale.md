# 1. From conversation to execution

This skill helps an agent preserve the user's decisions, formulate an outcome that can be verified, and carry the objective into the Goal tools available in its host. The language of a prompt alone cannot establish that work ran or succeeded.

## 1.1 Principles informed by practical use

| Failure pattern | Design response |
|---|---|
| A discussion ends with an attractive plan and no action | Confirm the Goal state, then begin a substantive first step within existing authorization. |
| A draft-only request unexpectedly starts work | Distinguish preparation from explicit execution requests. |
| New objective creation conflicts with an unfinished Goal | Read current state first; reuse a matching objective and surface a real conflict. |
| Passing functional checks conceal unmeasured quality | Keep acceptance dimensions separate and preserve every required outcome. |
| A save message is mistaken for successful recovery | Verify actual state transitions through the user workflow. |
| Repeated status reports consume the session | Look for changed artifacts, decision-relevant evidence, or a verified running process. |
| Interruptions lose decisions and retry history | Maintain compact recovery context in the project's existing records. |

These are generalized design cases. No private conversations, project names, local paths, or historical metrics are part of this public package.

# 2. References and adaptations

Sources reviewed on 2026-09-14. Links below track upstream main branches and may change. The instructions were independently written; this package does not bundle those projects' code or full skills.

| Primary source | Idea adopted | Adaptation |
|---|---|---|
| [Superpowers brainstorming](https://github.com/obra/superpowers/blob/main/skills/brainstorming/SKILL.md) | Turn discussion into an explicit design; scale process to scope. | Preserve existing execution authorization instead of adding a mandatory second approval for every task. |
| [Superpowers writing-plans](https://github.com/obra/superpowers/blob/main/skills/writing-plans/SKILL.md) | Organize tasks around inspectable deliverables. | Do not require full implementation code in every plan or a mandatory agent team. |
| [Superpowers verification-before-completion](https://github.com/obra/superpowers/blob/main/skills/verification-before-completion/SKILL.md) | Support completion claims with verification evidence. | Match evidence to the claim and its domain; repeat checks when evidence has become stale or the work changed. |
| [GSD verifier](https://github.com/gsd-build/get-shit-done/blob/main/agents/gsd-verifier.md) | Work backward from the promised outcome through artifacts, connections, and data flow. | Actual user-path evidence remains necessary; static presence and imports are insufficient for broad claims. |
| [GitHub Spec Kit analyze](https://github.com/github/spec-kit/blob/main/templates/commands/analyze.md) | Check requirement coverage, conflicts, ambiguity, and unmapped tasks. | Use a lightweight mapping inside the existing project structure. |
| [OpenSpec workflows](https://github.com/Fission-AI/OpenSpec/blob/main/docs/workflows.md) | Planning artifacts can change as implementation reveals new evidence. | Adapt the approach while preserving confirmed success criteria. |

These references informed specific workflow mechanisms. They do not establish compatibility with this host's Goal tools, and their popularity is not evidence of this skill's effectiveness.

# 3. Goal integration boundary

The host supplies `get_goal`, `create_goal`, and `update_goal` where available. Their live definitions govern supported actions and lifecycle rules. A compatible skill file does not make unavailable tools appear.

The skill checks existing state, handles conflicts, confirms creation by reading state back, and reports accurately when it continues outside a Goal. It never treats a plan file as proof that a Goal was created.
