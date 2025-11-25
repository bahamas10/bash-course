# Functions

## simple

``` bash
for name in foo bar baz; do
  ./greet "$name"
done
```

## using funcs

we can also use functions

``` bash
my-func() {
    echo hello from my function
    echo arg1 is $1
}

my-func
my-func hello!
my-func $1 $2 $3
my-func "$@"
```

### using arguments (local)

---
``` bash
my-func() {
    local arg1=$1
    echo hello from my function
    echo arg1 is $arg1
}

my-func
my-func hello!
my-func $1 $2 $3
my-func "$@"
```
---

## return codes

``` bash
my-func() {
    echo hi
    return 1
}

my-func
echo $?
```
