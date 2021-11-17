1. To show the whole path of working directory

Edit value of PS1. Common locations are ~/.profile, /etc/bash.bashrc, /etc/profile, ~/.bashrc, ~/.bash_profile. The system files are generally (but not always) run before the user files.

'''
export PS1="\[\033[01;32m\]\w\[\033[00m\]:\[\033[01;34m\](\$(git branch 2>/dev/null | grep '^*' | colrm 1 2))\[\033[00m\]\$ "
'''

2. To show the name of working directory alone

'''
export PS1="\[\033[01;32m\]\W\[\033[00m\]:\[\033[01;34m\](\$(git branch 2>/dev/null | grep '^*' | colrm 1 2))\[\033[00m\]\$ "
'''

3. To upgrade all outdated Python packages with pip

pip list --outdated --format=freeze | grep -v '^\-e' | cut -d = -f 1  | xargs -n1 pip install -U

https://stackoverflow.com/questions/2720014/how-to-upgrade-all-python-packages-with-pip
