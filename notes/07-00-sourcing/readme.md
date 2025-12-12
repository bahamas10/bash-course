# Sourcing Code

greet() {
}

greet dave
greet john

---

move the greet function into the lib/ dir

source it with `source` or `.`

source ./lib/greet
source -p ./lib greet

---

make lib have an example run

```
if ! (return 2>/dev/null); then
        # we are being called directly - execute the main function
        main "$@"
fi
```
