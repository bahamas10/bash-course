# Indexed Arrays

``` bash
array=(foo bar baz)

echo "$array"
```

``` bash
array=(foo bar baz)

echo "${array[0]}"
echo "${array[1]}"
echo "${array[2]}"

echo "${array[3]}"

echo "${array[-1]}"

item=2
echo "${array[item]}"
echo "${array[$item]}"

echo "${array[*]}"
echo "${array[@]}"
```

``` bash
array=(foo bar baz)

for item in "${array[*]}"; do
    echo "item is: $item"
done

for item in "${array[@]}"; do
    echo "item is: $item"
done
```

```
declare -a array=(...)
```

```
# array copy
newarray=( "${array[@]}" )
newarray=( "${array[@]:1}" )
newarray=( "${array[@]:0:2}" )
```

```
# array push
array=("${array[@]}" bat)
array+=(bat)
```

declare -p array < on the CLI
