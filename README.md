Run this in your project's source to clear local branches that are no longer on the remote

```bash
git fetch -p && git branch -vv | awk '/: gone]/{print $1}' | xargs git branch -D
```