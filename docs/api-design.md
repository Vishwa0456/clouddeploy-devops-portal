# CloudDeploy — API Design

## Auth
POST   /api/auth/register          — Register new user
POST   /api/auth/login             — Login, returns JWT
POST   /api/auth/logout            — Logout

## Projects
GET    /api/projects               — Get all projects for user
POST   /api/projects               — Create new project
PUT    /api/projects/:id           — Edit project
DELETE /api/projects/:id           — Delete project

## Deployments
POST   /api/deploy/upload          — Upload ZIP to S3
POST   /api/deploy/start           — Trigger deployment
GET    /api/deploy/status/:id      — Get deployment status
POST   /api/deploy/rollback        — Rollback to previous version
GET    /api/deploy/logs/:id        — Get deployment logs

## Dashboard
GET    /api/dashboard/stats        — Get all stats for dashboard
