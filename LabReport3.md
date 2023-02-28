The command I chose for this report is grep.


Option 1: -i

This option causes grep to perform a case-insensitive search. That means it will match patterns regardless of whether they are in upper or lower case.

Example 1.1:

```
grep -i 'PYTHON' ./written_2/languages.txt
```

Output:

```
Python
python
```

Explanation:  This command searches for lines in the languages.txt file in the ./written_2 directory that contain the word "PYTHON" (in any case), and it
prints those lines. In this case, it matches two lines that contain "Python" and "python" respectively. 
Example 1.2:

```
grep -i 'CAT' ./written_2/animals.txt
```

Output:

```
dog
CAT
```

Use-Case: Suppose you are looking for information about a certaincompany, but you're not sure if it's spelled with a capital or lowercase letter. You could use grep
-i 'company' to search for lines containing both "company" and "Company" in a file or directory.



Option 2: -r
This option causes grep to perform a recursive search. That means it will search for patterns not just in the specified file(s), but in all files and directories within the specified directory (and subdirectories).

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


Use-Case: Suppose you have a large directory with many subdirectories, and you want to find all files that contain a certain phrase. You could use grep -r 'phrase'
to search recursively through all the files in the directory and its subdirectories.



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
Option 4: -n
This option causes grep to print the line numbers along with the lines that match the pattern.

Example 4.1:

```
grep -n 'banana' ./written_2/fruits.txt
```

Output:

```
2:banana
```

Explanation: This command searches for lines in the fruits.txt file in the ./written_2 directory that contain the word "banana", and it prints those lines along
with their line numbers. In this case, it matches the line that contains "banana" and prints it along with its line number (which is 2).

Example 4.2:

```
grep -n 'python' ./written_2/*
```

Output:

```
./written_2/languages.txt:1:Python
./written_2/languages.txt:2:python
```

Explanation: This command searches for lines in all files in the ./written_2 directory that contain the word "python", and it prints those lines along with their
line numbers. In this case, it matches two lines - one in the languages.txt file, and another in the same file - and prints them along with their line numbers.

Use-Case: Suppose you are editing a file and you want to find and modify a specific line. You could use grep -n 'pattern' to find the line number of the line
containing the pattern, and then use a text editor to modify that line.



Option 5: -v
This option causes grep to print only the lines that do not match the pattern, rather than printing the lines that do match.

Example 5.1:

```
grep -v 'orange' ./written_2/fruits.txt
```

Output:

```
apple
banana
pear
```

Explanation: This command searches for lines in the fruits.txt file in the ./written_2 directory that do not contain the word "orange", and it prints only those
lines. In this case, it excludes the line that contains "orange" and prints the rest of the lines.

Example 5.2:

```
grep -v 'ruby' ./written_2/*
```

Output:

```
./written_2/animals.txt:dog
./written_2/animals.txt:cat
./written_2/fruits.txt:apple
./written_2/fruits.txt:banana
./
```

Explanation:This command searches for lines in all files in the ./written_2 directory that do not contain the word "ruby", and it prints only those lines. In this
case, it excludes the line that contains "ruby" (there is no such line) and prints all the other lines in the files.

Use-Case: Suppose you have a configuration file with many lines, and you want to see all the lines that don't include a certain keyword. You could use grep -v
'keyword' to exclude all lines that contain the keyword and show only the lines that don't contain it.



Source: chatGPT. ChatGPT prompt: "In what ways can I use the grep command to search through a directory"
