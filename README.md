# tuxies
Useful scripts, snippets and guidelines for common command line tasks

- [To count occurences of a character per line:](https://stackoverflow.com/questions/8629410/count-occurrences-of-character-per-line-field-on-unix)

```bash
awk -F 't' '{print NF-1, NR}'  input.txt
```


- [To select columns of a dataframe by name in bash:](https://unix.stackexchange.com/questions/25138/how-to-print-certain-columns-by-name)

Requirements:

```
pip install csvkit
```

```bash
cat test.csv

# outputs:
#id,age
#1,50
#2,70
```

```bash
csvcut -c "age"
# outputs:

#age
#50
#70
```
```bash
csvcut -c "id,age" test.csv | csvlook
# outputs:

| id | age |
| -- | --- |
|  1 |  50 |
|  2 |  70 |
```

which looks like a table:

| id | age |
| -- | --- |
|  1 |  50 |
|  2 |  70 |
