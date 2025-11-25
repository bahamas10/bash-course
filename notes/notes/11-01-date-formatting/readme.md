```
datefmt='%m/%d/%Y %H:%M:%S'
date "+$datefmt"

printf "%($datefmt)T\n" -1
date +'the time is %H:%M:%S'


printf '%T\n'
printf '%()T\n'
printf '%(%H:%M:%S)T\n' -1

printf '%(%H:%M:%S)T\n' -2

printf '%(%H:%M:%S)T\n' 0
printf '%(%H:%M:%S)T\n' 5000

date +%s
printf '%(%s)T\n' -1
printf -v var '%(%s)T\n' -1
echo $EPOCHSECONDS
echo $EPOCHREALTIME
```
