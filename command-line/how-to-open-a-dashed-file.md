In order to open a special character named file like `-`, we have to access the file
with full absolute system path. Otherwise `-` is usually considered as a normal
argument and it will not be treated as a file.

Example:
To open a dashed file in the current directory, we can do the following:

```
cat $(pwd)/-
```

- `pwd`: Print working(current) directory. Only when working with a file in current
  directory. To open a file in another directory we need to use absolute path.
