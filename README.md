# Few Setup I used for in my bash profile 
![GitHub branch checks state](https://img.shields.io/github/checks-status/dham6983/my-setup/main?style=plastic)
## Finding git branch during runtime
```bash
git_branch() 
{ 
   git branch 2>/dev/null | grep '^*' | colrm 1 2 
} 
```
## For nice view of git log
```bash
alias graph="git log --all --decorate --oneline --graph"
```
## Updating PS1
```bash
export PS1="[\d \t\[\033[36m\] \u@\h:\[\033[32m\]\w\[\033[33m\] \$(git_branch)\[\033[00m\]]$ "
```
