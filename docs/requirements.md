# CloudDeploy — Project Requirements

## User Module
- Register with name, email, password
- Login and receive JWT token
- Logout
- Forgot password

## Project Module
- Create a new project (name, runtime, environment)
- View all projects
- Edit project details
- Delete project

## Deployment Module
- Upload ZIP file
- Trigger deployment
- View deployment status (uploaded, deploying, success, failed)
- Rollback to previous version
- View deployment logs

## Dashboard
- Total projects count
- Total deployments count
- Successful deployments count
- Failed deployments count
- Currently running apps count

## Notifications Module
- Email notification on deployment upload
- Email notification on deployment start
- Email notification on deployment success
- Email notification on deployment failure
- Email notification on rollback
- Alert when EC2 CPU is high
- Alert when RDS storage is low
- Alert when Lambda throws errors
