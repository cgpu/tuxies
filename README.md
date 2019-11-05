# tuxies
Useful scripts, snippets and guidelines for common command line tasks

[To count occurences of a character per line:](https://stackoverflow.com/questions/8629410/count-occurrences-of-character-per-line-field-on-unix)

```bash
awk -F 't' '{print NF-1, NR}'  input.txt
```