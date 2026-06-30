# CloudDeploy — Database Design

## Aurora MySQL Tables

### users
| Column     | Type         |
|------------|--------------|
| id         | INT PK AUTO  |
| name       | VARCHAR(255) |
| email      | VARCHAR(255) |
| password   | VARCHAR(255) |
| created_at | TIMESTAMP    |

### projects
| Column       | Type         |
|--------------|--------------|
| id           | VARCHAR(36)  |
| user_id      | INT FK       |
| project_name | VARCHAR(255) |
| runtime      | VARCHAR(100) |
| environment  | VARCHAR(100) |
| created_at   | TIMESTAMP    |

### deployments
| Column      | Type        |
|-------------|-------------|
| id          | VARCHAR(36) |
| project_id  | VARCHAR(36) |
| version     | VARCHAR(50) |
| status      | VARCHAR(50) |
| duration    | INT         |
| deployed_at | TIMESTAMP   |

### deployment_logs
| Column        | Type        |
|---------------|-------------|
| id            | INT PK AUTO |
| deployment_id | VARCHAR(36) |
| log           | TEXT        |
| timestamp     | TIMESTAMP   |

## DynamoDB Tables

### DeploymentStatus
| Key       | Type   | Purpose                        |
|-----------|--------|--------------------------------|
| projectId | String | Partition key                  |
| timestamp | String | Sort key                       |
| status    | String | uploaded/deploying/success/failed |

### LiveLogs
| Key       | Type   | Purpose        |
|-----------|--------|----------------|
| projectId | String | Partition key  |
| logTime   | String | Sort key       |
| message   | String | Log message    |
