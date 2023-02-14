The command I chose for this report is grep.

The first command-line option I chose for this command is one I used recently in the skill demo. This command line can be used to search a directory for files that
contain a specified string and returns the number of those files present in said directory.
in the directory.

Example 1.1:

The first line:

we use the find function on a directory, and take the output and use ">" to place it into a file.

format:

```
find *file we want* > *file we want to put the output in*
```
our case:

```
"find written_2 > find-results.txt"
```

output:

The second line:

its the main grep, in which we use the grep command to choose the string we want to look for and where we want to look for it, in our case, we'd be looking in 
find-results.txt.

format:

```
grep *string we want to find* *file we want to find it in* > *file we want to put the output in*
```
our case:

```
grep ".txt" find-results.txt > grep-results.txt"
```

Third Line :

This lines utitilizes the "wc" command to return the number of files in a specified file.

format:

```
wc *file we want to look in*
```

our case:

```
wc grep-results.txt
```

output: 

```
224  224 11268 grep-results.txt
```

Example 1.2:

```
find written_2 > find-results.txt
grep ".pdf" find-results.txt > grep-results.txt
wc grep-results.txt
```

output(no pdf files in written_2):
```
0 0 0 grep-results.txt
```

The second command-line option I chose for this command is one I used recently in the skill demo. This command line can be used to recursively search a directory 
for files thatcontain a specified string. 

format:

```
grep -r *string*
```

Example 2.1:

```
grep -r Lucay
```

output:
returns a file that contains the word Lucayans

```
skill-demo1-data/written_2/travel_guides/berlitz2/Bahamas-History.txt
skill-demo1-data/written_2/travel_guides/berlitz2/Bahamas-Intro.txt
skill-demo1-data/written_2/travel_guides/berlitz2/Bahamas-WhatToDo.txt
skill-demo1-data/written_2/travel_guides/berlitz2/Bahamas-WhereToGo.txt
```

Example 2.2

```
grep -r water-sports
```

output:
returns multiple files that contain the string "water-sports"

```
written_2/travel_guides/berlitz1/WhatToJamaica.txt
written_2/travel_guides/berlitz1/WhatToLakeDistrict.txt
written_2/travel_guides/berlitz1/WhereToItaly.txt
written_2/travel_guides/berlitz2/Bahamas-Intro.txt
written_2/travel_guides/berlitz2/Vallarta-WhereToGo.txt
skill-demo1-data/written_2/travel_guides/berlitz1/WhatToJamaica.txt
skill-demo1-data/written_2/travel_guides/berlitz1/WhatToLakeDistrict.txt
skill-demo1-data/written_2/travel_guides/berlitz1/WhereToItaly.txt
skill-demo1-data/written_2/travel_guides/berlitz2/Bahamas-Intro.txt
skill-demo1-data/written_2/travel_guides/berlitz2/Vallarta-WhereToGo.txt
```

The third command-line option only displays the matched pattern and not the whole line containing the pattern. unlike command-line two, this only shows the word 
and the path instead of the whole file and the path.

format:

```
grep -r -o *string*
```

Example 3.1:

```
grep -r -o Lucayans 
```

output:

```
written-2/travel_guides/berlitz2/Bahamas-History.txt:Lucayans
written-2/travel_guides/berlitz2/Bahamas-History.txt:Lucayans
skill-demo1-data/written-2/travel_guides/berlitz2/Bahamas-History.txt:Lucayans
skill-demo1-data/written-2/travel_guides/berlitz2/Bahamas-History.txt:Lucayans
```
Example 3.2:

```
grep -r- o water-sports
```

output:

```
written_2/travel_guides/berlitz1/WhatToJamaica.txt:Lucayans
written_2/travel_guides/berlitz1/WhatToLakeDistrict.txt:Lucayans
written_2/travel_guides/berlitz1/WhereToItaly.txt:Lucayans
written_2/travel_guides/berlitz2/Bahamas-Intro.txt:Lucayans
written_2/travel_guides/berlitz2/Vallarta-WhereToGo.txt:Lucayans
skill-demo1-data/written_2/travel_guides/berlitz1/WhatToJamaica.txt:Lucayans
skill-demo1-data/written_2/travel_guides/berlitz1/WhatToLakeDistrict.txt:Lucayans
skill-demo1-data/written_2/travel_guides/berlitz1/WhereToItaly.txt:Lucayans
skill-demo1-data/written_2/travel_guides/berlitz2/Bahamas-Intro.txt:Lucayans
skill-demo1-data/written_2/travel_guides/berlitz2/Vallarta-WhereToGo.txt:Lucayans
```

The fourth Command-line option displays the line number of the matching pattern in each file. The output format is similar to command-line two, the difference is 
the line number is included between the path and the text.

format:

```
grep -r -n
```

Example 4.1

grep -r -n Lucayans

Output:

```
written-2/travel_guides/berlitz2/Bahamas-History.txt:6:
written-2/travel_guides/berlitz2/Bahamas-History.txt:7:
skill-demo1-data/written-2/travel_guides/berlitz2/Bahamas-History.txt:6:
```

Example 4.2:

grep -r -n water-sports

output:

```
written_2/travel_guides/berlitz1/WhatToJamaica.txt:76:
written_2/travel_guides/berlitz1/WhatToLakeDistrict.txt:94:
written_2/travel_guides/berlitz1/WhereToItaly.txt:3938:
written_2/travel_guides/berlitz2/Bahamas-Intro.txt:13:
written_2/travel_guides/berlitz2/Vallarta-WhereToGo.txt:133:
skill-demo1-data/written_2/travel_guides/berlitz1/WhatToJamaica.txt:76:
skill-demo1-data/written_2/travel_guides/berlitz1/WhatToLakeDistrict.txt:94:
skill-demo1-data/written_2/travel_guides/berlitz1/WhereToItaly.txt:3938:
skill-demo1-data/written_2/travel_guides/berlitz2/Bahamas-Intro.txt:13:
skill-demo1-data/written_2/travel_guides/berlitz2/Vallarta-WhereToGo.txt:133:
```


Sources for command-lines 1 and 2: class and lab. 
source for command-line 3 and 4: chatGPT. ChatGPT prompt: "In what ways can I use the grep command to search through a directory"
