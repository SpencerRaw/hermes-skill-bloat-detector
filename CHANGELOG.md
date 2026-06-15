# Changelog

## [1.2.0] — 2026-06-15

### Added
- **30-second health check** — one command for green/yellow/red verdict
- **Trigger conditions** — auto-load on Chinese phrases like 技能体检, 一键优化
- **Prerequisite checks** — verify gh auth + curator data before repair
- **Sustainable maintenance** — curator auto-clean + weekly cron + pre-create checklist
- **Quick decision tree** — 检测/一键优化/只分析 three entry paths

### Changed
- Frontmatter version → 1.2.0
- Consolidated "Phase 2 benchmark" as optional (static analysis usually sufficient)

### Fixed
- execute_code blocked in gateway → all scripts now terminal + python3 -c
- os.walk infinite recursion into .archive → added exclusion guard
- delegate_task can't test skill selection → documented limitation for T3/T5/T6

## [1.1.0] — 2026-06-15

### Added
- Real-world case study: 203→132 skills, 6→9 benchmark score
- One-click repair mode (一键优化)
- Archive recovery instructions
- Traps section (4 documented pitfalls from field use)

### Fixed
- Zombie archive script: added .archive exclusion for os.walk
- Hub-installed skill handling: archive-only, no structural edits

## [1.0.0] — 2026-06-15

### Added
- Initial release
- Four-phase detection: Inventory → Overlap → Benchmark → Diagnosis
- 7 degradation mechanisms documented
- 6-test benchmark suite
- P0→P3 tiered remediation
- 56 zombie skill identification pattern
