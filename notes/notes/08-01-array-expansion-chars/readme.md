```
for arg in $*; do
    echo "<$arg>"
done

for arg in "$*"; do
    echo "<$arg>"
done

for arg in $@; do
    echo "<$arg>"
done

for arg in "$@"; do
    echo "<$arg>"
done
```

arr=(foo bar baz)

```
for arg in ${arr[*]}; do
    echo "<$arg>"
done

for arg in "${arr[*]}"; do
    echo "<$arg>"
done

for arg in ${arr[@]}; do
    echo "<$arg>"
done

for arg in "${arr[@]}"; do
    echo "<$arg>"
done
```


If you find that it works without quotes - you're doing it wrong



- $*   - join items together as a string (separated by $IFS)
- "$*" - same as above with no word-splitting on expansion

- $@   - deconstruct array in the exact form of the array
- "$@" - same as above with no word-splitting on expansion
