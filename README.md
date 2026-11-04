# Useful Git Stuff

## Aliases
### Rebase current branch off of `origin/main`
```
alias.rebase-main=!git fetch origin main && git rebase origin/main
```
### Merge `origin/main` into current branch 
```
alias.merge-main=!git fetch origin main && git merge origin/main
```

### Reset current branch to origin/main
```
git config --global alias.reset-main '!f() { git fetch origin main && git reset --hard origin/main; }; f'
```
## Commands
### Disconnect local branch from origin:
```
git branch --unset-upstream
```
### Delete all local branches except main:
```
git branch | Select-String -NotMatch -Pattern "main" | %{ git branch -D $_.ToString().Trim() }`
```
