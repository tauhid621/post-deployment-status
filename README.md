# post-deployment-status
Posts deployment status in a slack channel using channel web-hook secret

## Usage
- Success

```
on: workflow_dispatch

jobs:
  build:
    runs-on: ubuntu-latest
    steps:
    - uses: Internal-Actions/post-deployment-status@main
      env:
        DEP_STATUS: success
        SLACK_CHANNEL_SECRET: ${{ SECRETS.SLACK_CHANNEL_SECRET }}
```
        
- Failure        
```
on: workflow_dispatch

jobs:
  build:
    runs-on: ubuntu-latest
    steps:
    - uses: Internal-Actions/post-deployment-status@main
      env:
        DEP_STATUS: failure
        SLACK_CHANNEL_SECRET: ${{ SECRETS.SLACK_CHANNEL_SECRET }}
```
