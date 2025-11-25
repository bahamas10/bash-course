# For loops

``` bash
for name in foo bar baz; do
    echo "name is $name"
done
```

``` bash
for c in {a..f}; do
    echo "c is $c"
done
```

``` bash
for i in {1..5}; do
    echo "i is $i"
done
```

``` bash
max=5
for i in {1..$max}; do
    echo "i is $i"
done
```

``` bash
max=5
for ((i = 0; i < max; i++)); do
    echo "i is $i"
done
```
