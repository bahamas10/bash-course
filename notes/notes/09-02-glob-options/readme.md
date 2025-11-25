```
mkdir empty
ls empty
ls empty/*

printf '<%s>\n' empty/*

touch empty/foo

printf '<%s>\n' empty/*

rm empty/foo

printf '<%s>\n' empty/*

shopt -s nullglob

printf '<%s>\n' empty/*
arr=(empty/*)

echo "${arr[*]}"

---

ls empty/*

shopt -u nullglob
```

---


```
touch empty/.hidden-file

ls empty
ls -a empty

echo empty/*

shopt -s dotglob

echo empty/*

arr=(empty/*)
echo "${arr[*]}"

shopt -u dotglob

arr=(empty/* empty/.*)
echo "${arr[*]}"

shopt -s dotglob
echo empty/* empty/.*
```

---

```
cd ~/dev/ysap

find .
echo **

shopt -s globstar

echo **
printf '%s\n' **

shopt -s dotglob

txt=( ./**/*.txt )

count it, show loop
```
