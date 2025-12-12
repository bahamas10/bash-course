# Curlies vs. Parens

``` bash
greet() {
	name=$1
	echo "hello $name!"
}

echo "before: $name"
greet dave
echo "aftire: $name"
```

1. run it
2. swap { to (
3. explain local
4. remove local, force with `( greet dave )`

---

output=$(greet dave)
echo "output=$output, name=$name"

output=${ uname; }
echo "output=$output, name=$name"

{ echo hi; whoami; id; } | nl
( echo hi; whoami; id ) | nl
