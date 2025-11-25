show bomb.txt

unminify it

show the diagram

explain why it's a problem and isn't specific to bash

---

```
#!/usr/bin/env bash

bomb() {
        local num=$1
        local name=$2
        printf '%-2d %-5s %s\n' "$num" "$name" 'running' >&2

        if ((num == 6)); then
                return 0
        fi

        ((num++))
        bomb "$num" 'left' | bomb "$num" 'right' &
}

bomb 0 'none'
```

./step-bomb 2>&1 | sort | awk '{print $1}' | uniq -c

bc
2^5
2^6

---

RUN IT
