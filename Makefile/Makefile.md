# Makefile

* Filename: `Makefile`

* Indent **must** be `tab`

## Shell Scripts

```makefile
[make-command]:
	put shell scripts here
```

e.g.,

```makefile
commit:
	git add docs && git commit -m ':rocket: Launch site' && git push origin HEAD
```

### Chaining make commands

```makefile
[make-command]: [make-command1] [make-command2]
```

e.g.,

```makefile
build:
	yarn build
commit:
	git add docs && git commit -m ':rocket: Launch site' && git push origin HEAD

deploy: build commit
```
