# sed, awk, and grep

cat /etc/passwd
man 5 passwd

cut for names
remove comments
find dave with grep

use sed to replace shell

cat /etc/passwd | grep nobody | cut -d : -f 7 | sed 's|/usr/bin/|/tmp/sbin/|'


cat /etc/passwd | awk -F : '/^[^#]/ { printf("the shell is %s\n", $7); }'


cat /etc/passwd | awk -F : '/^[^#]/ { print $7 }' | sort | uniq -c | sort -n


cat /usr/share/dict/words | grep dave | wc -l
cat /usr/share/dict/words | grep -c dave
grep -c dave /usr/share/dict/words


man ls
man ls | grep dave
man ls | grep file
man ls | grep file | wc -w
man ls | grep file | wc -l
man ls | grep file | wc
