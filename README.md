## Few Setup I used for in my bash profile 
# finding git branch during runtime
git_branch() {
  git branch 2>/dev/null | grep '^*' | colrm 1 2
}

# for noce view of git log
alias graph="git log --all --decorate --oneline --graph"

# updating PS1
export PS1="[\d \t\[\033[36m\] \u@\h:\[\033[32m\]\w\[\033[33m\] \$(git_branch)\[\033[00m\]]$ "
