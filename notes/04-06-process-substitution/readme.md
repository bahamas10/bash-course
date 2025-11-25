```
words=$(grep d /usr/share/dict/words)

i=0
for word in $words; do
  echo "$word"
  ((i++))
done

echo "found $i words"
```

```
words=$(grep d /usr/share/dict/words)

i=0
while read -r word; do
  echo "$word"
  ((i++))
done <<< "$words"

echo "found $i words"
```

```
i=0
grep d /usr/share/dict/words | while read -r word; do
  echo "$word"
  ((i++))
done

echo "found $i words"
```

```
i=0
while read -r word; do
  echo "$word"
  ((i++))
done < <(grep d /usr/share/dict/words)

echo "found $i words"
```
