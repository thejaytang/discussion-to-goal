# Validation scope

Release candidate: 0.1.0. Checks performed on 2026-09-14.

| Check | Evidence and scope |
|---|---|
| Skill structure | The Codex skill-creator validator returned `Skill is valid!`. |
| Discovery metadata | Parsed YAML; checked description length and explicit skill mention in the default prompt. |
| English/Chinese parity | Independent read-only review found no material mismatch in installation, usage, permissions, or capability claims. |
| Public package content | Inspected the file list and scanned for personal paths, private project names, conversation markers, and credential patterns. No matches found. |
| Local documentation links | Checked relative file and asset targets. |
| Cover graphics | Parsed both SVG files and visually inspected English and Chinese browser renders. |
| Source behavior scenarios | Six side-effect-free simulations covered execution, draft-only output, existing-Goal conflict, incomplete acceptance, skill design, and unavailable Goal tools for a manuscript task. A conflict-handling wording issue was corrected. |

No live business Goal was created during these checks. Simulation, valid packaging, and readable documentation are not proof of effective Goal execution on another installation.

Remote installation and rendered GitHub navigation are checked during publication; confirmed results are recorded here before the release archive is finalized.
