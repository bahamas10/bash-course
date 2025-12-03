# User Input

Modify the above 2 scripts to take from stdin

``` bash
read -p 'enter your name: ' name
echo hello $name
```

...

Then modify to take as an argument

``` bash
name=$1
echo "hello $name"
```

Show what happens without an argument:

``` bash
if [[ -n $1 ]]; then
  name=$1
else
  read -p 'enter your name: ' name
fi
...
```

Show `help [[` and `help test`

- Arguments

``` bash
for thing in "$@"; do
    echo thing is $thing
done
```
