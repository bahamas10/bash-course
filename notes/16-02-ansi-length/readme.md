# Pitfall: String Length

```
echo $"\e[33mHello World\e[0m"
echo $'\e[33mHello World\e[0m'

s=...

echo "${#s}"

echo "$s"
echo "$s" | wc -c
echo -n 'Hello World' | wc -c
```

mention strip ansi
