# Git workflow

## Create your own branch to work on

- Before begin work, you should have a cloned repository using `git clone`
- `git checkout -b [branch name]` will create a branch
- `git branch -a` shows what branch you're on

## Update your local repo daily

Every morning, you should update your local repo to mirror the master.
- Navigate to your local repo and run `git checkout master` and then `git pull`
- Then go back to `git checkout [branch name]`

> Tip: If you have conflicts that can't auto-merge, run `git merge master`

## Push your branch

When you are ready, navigate to the highest level dir with your changes and enter `git add .`
Run `git commit -m "[remarks]"`
Because you did not set upstream branch, you'll have to run `git push --set-upstream origin [branch name]`

> Tip: If you had set an upstream branch in the beginning steps, you could have run `git push` instead.

## Side Quest: Directory Copy Automation

How to clone a directory i many times and append number to dir name
```
for i in {10..50}; do cp -r class-template/* class-$i; done
```
