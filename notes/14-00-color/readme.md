```
echo '<bold>hello</bold>'
echo -e '\e[1mhello'

# break it down

echo $'\e[1mhello'
echo $'\033[1mhello'
echo $'\x1b[1mhello'

x1b == 033 == 27 decimal
https://www.ascii-code.com

ansi_escape=$'\e'
echo "${ansi_escape}[1mHello World"

tput bold; echo hi

tput bold; echo hi; tput sgr0
echo -e '\e[1mhello\e[0m'


tput setaf 1; echo hi
tput setaf 2; echo hi
tput setaf 3; echo hi

echo -e '\e[31mhi'

printf '\e[38;5;nmHello'
printf '\e[38;5;128mHello\n'

reference https://gist.github.com/fnky/458719343aabd01cfb17a3a4f7296797

colors () {
    local i
    for i in {0..255}; do
        printf '\e[38;5;%dmcolor %d\n' "$i" "$i";
    done
    printf '\e[0m'
}
```
