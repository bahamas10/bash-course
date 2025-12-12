# Conditionals

we can check things internal to bash

``` bash
a=2
b=2
if [[ $a == $b ]]; then
    echo they are the same
fi
```

we can check the outside world

``` bash
if [[ -f /etc/passwd ]]; then
    echo /etc/passwd is a file
fi
```

we also have `while` and `until`

``` bash
while [[ -f flag.txt ]]; do
    rm flag.txt
done
echo done
```

``` bash
until [[ -f flag.txt ]]; do
    touch flag.txt
done
echo done
```


---

these are just COMMANDS

``` bash
if true; then
    echo hi
fi
```

```
while ls; then
    sleep 1
fi
```

```
[[ -f /etc/passwd ]]
echo $?
[[ -f /etc/passwd ]] && echo it exists
```
