# Parameter Expansion

== casing ==

``` bash
s='dave eddy'
${s^}
${s^^}
${s^^d}
${s^d}
${s^^da}
${s^^[da]}
${s,,}
s='DAVE EDDY'
${s,,}
${s,}
${s,,D}
${s,D}
${s,,DA}
${s,,[DA]}
```

== default values ==

``` bash
name=$1

echo "hello $name!"

echo 'done'
```

```
name=${1:-dave}
name=${1:-$USER}

name=${1?}
name=${1?You must supply a name}
name=${1:?}
name=${1:?You must supply a name}
```

== replacements ==

```
path=/home/dave/abc.txt

echo "$path" | tr a o
echo "${path/a/o}
echo "${path//a/o}

basename "$path"
dirname "$path"

echo "${path}"
echo "${path#*/}"
echo "${path##*/}"

echo "${path}"
echo "${path%/*}"
```

```
echo "${path//[abc]/5}"
```

== substrings ==

s='dave eddy'

echo "${s:0}"
echo "${s:1}"
echo "${s:2}"
echo "${s:3}"

echo "${s:-1}"
echo "${s: -1}"
echo "${s: -2}"

echo "${s:0:1}"
echo "${s:1:2}"
echo "${s:2}"
echo "${s:3:-1}"


Loop character by character

s='dave eddy'
len=${#s}

for ((i = 0; i < len; i++)); do
    c=${s:i:1}
    echo "$c"
done



== arrays ==

```
arr=(foo bar baz)

printf '<%s>\n' "${arr[@]}"
printf '<%s>\n' "${arr[@]:1:1}"

$ printf '<%s>\n' "${arr[@]/a/1}"
$ printf '<%s>\n' "${arr[@]#b}"
$ printf '<%s>\n' "${arr[@]%z}"
