# Git Repo Sync

```yaml
name: <action-name>

on: 
  - push
  - delete

jobs:
  sync:
    runs-on: ubuntu-latest
    name: Git Repo Sync
    steps:
    - uses: actions/checkout@v2
      with:
        fetch-depth: 0
    - uses: pawan-59/git-test@v0.1.0
      with:
        # Such as https://github.com/pawan-59/git-repo-sync.git
        target-url: <target-url>
        # Such as wangchucheng
        target-username: <target-username>
        # You can store token in your project's 'Setting > Secrets' and reference the name here. Such as ${{ secrets.ACCESS_TOKEN }}
        target-token: <target-token>
```
