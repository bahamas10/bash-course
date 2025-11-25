``` bash
thing='whatever'

echo "thing is $thing"
```

```
thing=`whoami`
thing=`ls`

thing=$(whoami)

# contrived example, use
thing=$USER

# we prefer $(...) because nesting weirdness)

whoami
echo `whoami`
echo `echo \`whoami\``
echo `echo \`echo \\\....
echo "`echo \`"

whoami
echo "$(whoami)"
echo "$(echo "$(whoami)")"
echo "$(echo "$(echo "$(whoami)")")"

# don't let me catch you writing code like this

```

```
my-func() {
    echo hi
}

thing=$(my-func)

echo "thing is $thing"
```

```
i=5
my-func() {
    i=6
    echo hi
}

thing=$(my-func)

echo "thing is $thing"
```
