# V12.6 Visible Enterprise Implementation Notes

This build makes the requested upgrade visible from the frontend dashboard.

## Visible in Dashboard
- Workspace Ops tab preserving old operational KPIs and today focus.
- Executive Command tab with portfolio health, SLA/overdue, blockers, AI actions, project delivery map and AI investigation notes.
- Analytics tab with burn-up/burn-down trend, productivity trend, workload matrix, stage distribution and risk radar.
- Gantt / Roadmap tab with roadmap bars and dependency/critical path panel.
- PM Power Tools tab for sprint planning, backlog grooming, templates, milestones, RID log, release readiness and approvals.
- AI Copilot tab for health summary, what changed today, risk prediction, requirement-to-tasks, meeting notes-to-tasks, sprint summary, delay detection, status mail and RCA.
- Collaboration tab for mentions, threaded comments, rich editor, activity timeline, file/voice notes, realtime hooks, read receipts, team availability and daily standup.
- Admin & Security tab for CORS, CSRF, RBAC, audit, device trust, workspace policy, password/data retention and impersonation audit planning.
- Feature Matrix tab listing all requested features and their current implementation state.

## Important honesty
Some features are now visible UI/workflow shells and not yet fully DB-backed engines. Items such as full CSRF middleware, backend RBAC policy engine, Alembic migrations, true dependency schema, real LLM execution, local bundling and full file modularization require deeper backend/schema refactoring beyond a quick UI patch.

## Theme handling
The new dashboard uses CSS variables plus explicit `.dark` handling for dark/light mode so the Command Center changes theme more reliably.
