# How to pipe `find` with `cat`?

Sometimes when you want to `find` a specific file somewhere inside a directory
and wants to read it's content via `cat`. Here is how to do so:

```sh
find . -type f -size 1004c -exec cat {} +
```

- `find .` - search only in the current directory.
- `-type f` - find only files.
- `-size 1004c` - find only files with size of 1004 bytes. The `c` stands for `bytes`.
- `-exec cat {} +` - execute `cat` on each found file. When `+` is used, it will
find groups the file paths together and passes them to `cat` at once. if `\;` is
used, it will execute `cat` on each file separately. So using `+` reduces the
overhead of starting a new process for each file, which can be significant when
dealing with a large number of files.
