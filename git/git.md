# Git  

Git is a source control program.

## Initializing a git repo and pushing to Github
```bash
git init
git add -A
git commit -m "First commit"
git add origin https://github.com/username/reponame
git push -u origin master
```

## Make new local branch and push to remote

```
git checkout -b branchname
git push origin branchname
```

## Checkout remote branch

```
git checkout --track origin/branchname
```

## Check difference between branches

```bash
git diff [branch1] [branch2]
```
