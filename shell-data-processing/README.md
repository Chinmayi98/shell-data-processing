# Shell Data Processing Notes

## Common Commands

- To make a new directory
``` 
mkdir 
```
- To change to a directory 
``` 
cd 
```
- To make an empty new item 
``` 
ni 
```
- To list the contents 
``` 
ls 
```
- To close the PowerShell window
``` 
ALT SPACE C 
```

## Client URL (CURL) Commands

- To return text from a page by using a custom URL
``` 
curl "url" 
```

- To return the page text and output it to a file
``` 
curl "yourlongurl" -O "data.txt" 
```

- May need to use this command to request content from an HTTPS url
``` 
[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12 
```

## Bash Commands

- To transform each space (' ') into a return character ('\12')
``` 
tr ' ' '\12' <returnedfile 
```

- To pipe the output to sort
``` 
tr ' ' '\12' <returnedfile | sort 
```

- To pipe the output that is sorted to uniq -c for counting
``` 
tr ' ' '\12' <returnedfile | sort | uniq -c 
```

- To pipe the reduced output to sort with -nr (n stands for numeric and r stands for reverse) flag
``` 
tr ' ' '\12' <returnedfile | sort | uniq -c | sort -nr 
```

- To redirect the output to a text file
``` 
tr ' ' '\12' <returnedfile | sort | uniq -c | sort -nr > result.txt 
```
