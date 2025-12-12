# Associative Arrays

``` bash
declare -A arr
echo $?
```

``` bash
declare -A array || exit

if ! declare -A array; then
    echo uh oh
fi
```

``` bash
declare -A array=()

array[foo]=1
array[bar]=2
array[baz]=3

echo "$array" # nothing
echo "${array[foo]}"
echo "${array[bar]}"
echo "${array[fake]}"

echo "${array[*]}"
echo "${array[@]}"

echo "${!array[*]}"
echo "${!array[@]}"

for key in "${!array[@]}"; do
    value=${array[$key]} # $ is needed
    echo "$key is $value"
done
```
