# Braces and Globbing

```
mkdir files
echo files/{foo,bar,baz}.{jpg,txt}
touch files/{foo,bar,baz}.{jpg,txt}

printf '<%s>\n' files/*.txt

# explain that it doesn't have to exist - compare to ext glob
printf '<%s>\n' files/{foo,bar}.txt
printf '<%s>\n' files/@(foo|bar).txt

ls files/*.{txt,jpg}


mkdir empty
ls empty/*.{txt,jpg}
printf '<%s>\n' empty/*.{txt,jpg}
```
