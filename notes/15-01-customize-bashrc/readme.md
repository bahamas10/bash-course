# Customizing Bash

```
1. shopt -s cdspell
# show examples of types

2. shopt -s autocd
# show examples of autocd

3. talk about `..`

4. mention that it's interactive only
```

```
# Aliases (if applicable)
grep --color=auto < /dev/null &>/dev/null &&
    alias grep='grep --color=auto'
xdg-open --version &>/dev/null &&
    alias open='xdg-open'
command -v system_profiler &>/dev/null &&
    alias wattage='system_profiler SPPowerDataType | grep Wattage'

# Enable color support of ls
if ls --color=auto &>/dev/null; then
        alias ls='ls -p --color=auto'
else
        alias ls='ls -p -G'
fi
```

make our own bashrc
