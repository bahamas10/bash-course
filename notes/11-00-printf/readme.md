# Understanding printf
```
s='hello world'

echo "$s"

printf "$s" # wrong
printf '%s\n' "$s" # right

printf '>>> the string is: %s!! <<' "$s"

$ printf '%5s %5s\n' hello world
hello world
$ printf '%5s %5s\n' a b
    a     b
$ printf '%-5s %-5s\n' a b
a     b
$ printf '>>%*s<<\n' 20  dave
>>                dave<<


$ printf '%d\n' 55
55
$ printf '%5d\n' 55
   55
$ printf '%-5d\n' 55
55
$ printf '%05d\n' 55
00055

$ printf '%d\n' hello
-bash: printf: hello: invalid number
0
$ printf '%d\n' 05
5
$ printf '%d\n' 06
6
$ printf '%d\n' 07
7
$ printf '%d\n' 08
-bash: printf: 08: invalid octal number
0
# check exit code

$ printf '%d\n' 09
-bash: printf: 09: invalid octal number
0
$ printf '%d\n' 010
8
$ printf '%d\n' 011
9
$ printf '%d\n' 0xff
255


$ printf '%q\n' 'foo$bar'
foo\$bar

$ printf 'hello%bworld\n' '\x0a'
hello
world
```
