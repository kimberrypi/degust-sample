This repository is an example of running degust.py to generate an HTML file.
Reference repository: [degust](https://github.com/drpowell/degust)

# Displaying Available commands
`python degust.py --help`

Running this command displays all the available arguments for `degust.py`:

| positional arguments: |                                     |
| --------------------- | ----------------------------------- |
| csvfile               | CSV file to process (default stdin) |

---

| optional arguments: |                                                                                                           |
| ------------------- | --------------------------------------------------------------------------------------------------------- |
| -h, --help          | show this help message and exit                                                                           |
| -o OUT, --out OUT   | Output file (default stdout)                                                                              |
| --name NAME         | Name for this DGE comparison                                                                              |
| --notour NOTOUR     | Do not show the tour on first load                                                                        |
| --primary PRIMARY   | Name for the primary condition that the fold-changes are relative to                                      |
| --avg AVG           | Name for average intensity column in CSV file                                                             |
| --fdr FDR           | Name for "FDR" column in CSV file (default "adj.P.Val")                                                   |
| --logFC LOGFC       | Comma separated names for "logFC" columns in CSV file                                                     |
| --info INFO         | Comma separated names for info columns in CSV file                                                        |
| --counts COUNTS     | Specify 'count' columns - only used for display in the table. Specify the name of the logFC column then a |
                       colon followed by comma separate count columns. Use
                       multiple times for multiple conditions. Example:
                       --counts cond1:cond1-rep1,cond1-rep2|
 | --link-col LINK_COL  |Name for column to use with "--link-url"|
 | --link-url LINK_URL  |Gene info URL. Used when double-clicking the gene-table. Any "%s" will be replaced with the value from the specified "--link-col"|
  | --tab     |           Specify that the csv file is actually tab delimited|
  | --cuffdiff |          Input file is from cuffdiff (gene_exp.diff). This will set the columns automatically. Note this is still
                       experimental|

optional arguments can be used to identify the name of the column required in your csv file

# Sample command
```python
python degust.py degust-1.csv --avg AveExpr --fdr FDR --logFC Keap1KO --info symbol --out index.html
```
