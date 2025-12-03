# Arithmetic Expression

``` bash
echo $((2 + 2))
echo $((18))

a=2
b=3

echo $(($a + $b))
echo $((a + b))

a='hello'
b='goodbye'
echo $((a + b))


i=0
((i++))
echo "$i"

((i = i + 1))
((i = 57))

((2 + 2))
echo $?

((2 - 2))
echo $?

((a = 5, b = 7))
```

---

``` bash
a=06
echo $a
echo $(( a ))

a=07
echo $(( a ))

a=08
echo $(( a ))
echo $(( 10#a ))
echo $(( 10#$a ))
```
