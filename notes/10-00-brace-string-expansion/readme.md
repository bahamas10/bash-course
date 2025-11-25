```
echo {hello,world}

echo "{hello,world}"



echo my-file.{txt,jpg,mov}

filename='my-file'
echo "$filename."{txt,jpg,mov}


# make script
filename='my-file'
array=("$filename."{txt,jpg,mov})

for item in "${array[@]}"; do
	echo "$item"
done

# make script

array=(/etc/{foo,bar,baz}/{1,2,3}.txt)
echo "${#array[@]} items"
for item in "${array[@]}"; do
	echo "$item"
done
```
