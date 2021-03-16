# Few Setup I used in my bash profile 
![GitHub Workflow Status](https://img.shields.io/github/workflow/status/dham6983/my-setup/CI%20for%20Setup%20file?label=my-build&logo=Github&style=plastic) ![GitHub repo size](https://img.shields.io/github/repo-size/dham6983/my-setup?style=plastic)
## Finding git branch during runtime
```bash
git_branch() 
{ 
   git branch 2>/dev/null | grep '^*' | colrm 1 2 
} 
```
## Updating PS1
```bash
export PS1="[\d \t\[\033[36m\] \u@\h:\[\033[32m\]\w\[\033[33m\] \$(git_branch)\[\033[00m\]]$ "
```

## For nice view of git log
```bash
alias graph="git log --all --decorate --oneline --graph"
```

