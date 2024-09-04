# How to show all unique lines in a text file?

> Alternate title: How to filter out duplicate lines from a text file?

```sh
sort log.txt | uniq -u
```

- `sort` : This sorts the contents of the file in lexicographical order(Dictionary order)
- `uniq -u` : This filters the sorted output, displaying only the lines that are unique.

> [!NOTE]
> `sort` is important because `uniq` only filters out the duplicate adjacent/consecutive
> duplicate lines. If the line appears later in the file, `uniq` itself won't filter it out.
