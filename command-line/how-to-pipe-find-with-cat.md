Sometimes when you want to `find` a specific file somewhere inside a directory
and wants to read it's content via `cat`. Here is how to do so:

```sh
find -type f -size c1004 -exec cat {} +
```
