# my-setup
Setup I used for developments
==== bash profile setup ===
git_branch() {
  git branch 2>/dev/null | grep '^*' | colrm 1 2
}
alias graph="git log --all --decorate --oneline --graph"
export PS1="[\d \t\[\033[36m\] \u@\h:\[\033[32m\]\w\[\033[33m\] \$(git_branch)\[\033[00m\]]$ "
