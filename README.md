# Useful Git Commands that I frequently use but never seem to remember

- Disconnect local branch from origin: `git branch --unset-upstream`
- Delete all local branches except main:
``` git branch | Select-String -NotMatch -Pattern "main" | %{ git branch -D $_.ToString().Trim() } ```
