# Find Command

``` bash
find .

find /var/empty
find /var/empty -type f

find /usr/share -type f | wc -l
find /usr/share -type d | wc -l
find /usr/share -type l | wc -l
# add them up


find /usr/share/ -type f -name '*.plist' -iname 'info*'
find /usr/share/ -type f -name 'Info.plist' -exec echo the file is {} \;

echo /usr/share/*
for f in ...; do
```

we'll talk more about that in the globbing section
