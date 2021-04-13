1. To show the whole path of working directory

export PS1="\[\033[01;32m\]\w\[\033[00m\]:\[\033[01;34m\](\$(git branch 2>/dev/null | grep '^*' | colrm 1 2))\[\033[00m\]\\$ "

2. To show the name of working directory alone

export PS1="\[\033[01;32m\]\W\[\033[00m\]:\[\033[01;34m\](\$(git branch 2>/dev/null | grep '^*' | colrm 1 2))\[\033[00m\]\\$ "
