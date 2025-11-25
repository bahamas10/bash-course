```
uname
echo $?
```

- show what happens
 - explain output vs return code
- capture output in a variable
- capture exit code in a variable
- replace with my-func

```
my-func() {
	echo hello
	return 0
}

my-func
echo $?
```

- show what happens
 - explain it's like a mini program

```
my-func() {
	echo this goes to stdout >&1
	echo this goes to stderr >&2
	return 0
}

output=$(my-func)
output=$(my-func 1>/dev/null)
output=$(my-func 2>/dev/null)
output=$(my-func 2>&1)

output=$(my-func >/dev/null 2>&1)
output=$(my-func 2>&1 >/dev/null)
```
