# 🚀 CI/CD Pipelines in Azure DevOps

## ⚙️ Pipeline Overview
Our pipelines ensure that every change is tested and validated before it reaches production.

### The Pipeline Lifecycle
`Trigger` $\rightarrow$ `Build` $\rightarrow$ `Test` $\rightarrow$ `Deploy`

## 🧪 Testing Suite Integration
The most critical part of the pipeline is the **Test Stage**.

### YAML Example: Running Tests
```yaml
trigger:
  - main
  - feature/*

pool:
  vmImage: 'ubuntu-latest'

steps:
- task: NodeTool@0
  inputs:
    versionSpec: '18.x'

- script: npm install
  displayName: 'Install Dependencies'

- script: npm run test
  displayName: 'Run Unit Tests' # This is where Jest/Mocha/etc. run

- task: PublishTestResults@2
  condition: succeededOrFailed()
  inputs:
    testResultsFormat: 'JUnit'
    testResultsFiles: '**/test-results.xml'
```

## 🛠️ Common Pipeline Tasks
| Task | Purpose |
| :--- | :--- |
| `NodeTool` | Sets the Node.js version for the agent |
| `Docker@2` | Build and push images to Azure Container Registry |
| `PublishTestResults` | Surfaces test failures directly in the ADO PR UI |
| `PublishBuildArtifacts` | Saves the build output for deployment |

## 🚨 Handling Failures
1.  **Check Logs:** Click on the failed task to see the console output.
2.  **Local Reproduction:** Try to run the exact command (e.g., `npm run test`) locally.
3.  **Fix & Push:** Push a fix to your feature branch; the pipeline will trigger automatically.
