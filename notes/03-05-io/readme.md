# Input / Output

Bash can take input from the user

``` bash
read -r foo
echo "you said: $foo"
```

./script
echo hi | ./script

cat /usr/share/dict/words | ./script

``` bash
while read -r line; do
    echo "got line: $line"
done
```

talk about how the read command is in the condition of the while loop

---

# talk about how these are the same
cat /usr/share/dict/words | ./script
< /usr/share/dict/words ./script
./script < /usr/share/dict/words
