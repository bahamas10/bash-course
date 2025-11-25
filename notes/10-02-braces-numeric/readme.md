```
echo {1,2}
echo {1..2}
echo {1..20}
echo {5..10}
echo {10..5}
echo {1..100..5}

seq 1 10
seq 1 20
seq 5
seq 1 20 5 # wrong
seq 1 5 20 # wrong

for i in $(seq 1 10); do
	echo "$i"
done

for i in {1..10}; do
	echo "$i"
done

---

for i in foo {1..4} {8..10} bar; do
	echo "$i"
done

for i in {1..10..3}; do
	echo "$i"
done


max=4
for i in {1..$max}; do
	echo "$i"
done

max=4
for i in $(seq 1 "$max"); do
	echo "$i"
done

max=4
for ((i = 1; i <= max; i++)); do
	echo "$i"
done
```
