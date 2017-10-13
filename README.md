# git-branch-sync
How to sync file changes between two branches

## Useful git commands
- Add files to repo `git add .`
- Commit changes `git commit -m "message"`
- Pull changes from remote `git pull origin/<branch-name>`
- Push changes to remote `git push origin <branch-name>`
- Create new branch `git branch new-branch-name`
- Switch branch `git checkout new-branch-name`
- Cherry-pick a commit from other branch and applay it to current `git cherry-pick <commit-id>`

## Cherry-picking conflict
If we cherry-pick a commit from 'master' that has changes on the same line as the current branch,
we get a conflict which we can resolve manually:
```
<!-- feature-one: index.html -->

<body>
  <div class="container">
    <h1>Git Branch Sync</h1>
    <p>Firts paragraph</p>
<<<<<<< HEAD
    <p>Feature-one paragraph</p>
=======
    <p>Master paragraph</p>
>>>>>>> 416c9ef... add master paragraph
  </div>
</body>
```