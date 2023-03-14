The command I chose for this report is grep.


Option 1: ```-i```

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



Option 2: ```-r```


This option causes grep to perform a recursive search. That means it will search for patterns not just in the specified file(s), but in all files and directories
within the specified directory (and subdirectories).

format:


```
grep -r *string*
```


Example 2.1:


```
grep -r Lucay
```


Output:
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


Option 3: ```-o```


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
Option 4: ```-n```


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



Option 5: ```-v```


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


Option 6: ```-w```

This option causes grep to match whole words only. For example, if you search for the word "the" using grep 'the', it will match lines containing words like "then"
and "there", which may not be what you want. However, if you use grep ```-w``` 'the', it will match only lines containing the word "the".

Examples 6.1:

```
grep -w 'the' ./written_2/text.txt
```

Output:

```
The quick brown fox jumps over the lazy dog.
```

This command searches for lines in the text.txt file in the ./written_2 directory that contain the whole word "the", and it prints those lines. In this case, it
matches the only line in the file that contains the whole word "the".

Example 6.2:

```
grep -w 'apple' ./written_2/fruits.txt
```

Output:

```
N/A
```

This command searches for lines in the fruits.txt file in the ./written_2 directory that contain the whole word "apple", and it prints those lines. In this case,
there are no lines in the file that contain the whole word "apple", so the output is empty.

Use-case:

You want to search for a specific word, but you don't want to match on substrings or partial matches. For example, you might use ```-w``` to search for occurrences
of the word "cat", but not match on words like "catch", "caterpillar", or "category". 


Option 7: ```-B```

The -B option tells grep to print a specified number of lines before each match. This can be useful when you want to see the context around each match, such as when
troubleshooting an issue in a log file. By default, grep will print the entire line containing the match, but you can use -o to print only the matching portion of
the line. You can also use -A to print lines after the match in addition to the lines before it.

Example 7.1:

```
grep -B 2 'error' log.txt
```

output:

```
2023-02-25 14:03:42 - ERROR - Failed to connect to database
2023-02-25 14:03:41 - INFO - Starting application
2023-02-25 14:03:40 - INFO - Initializing database connection
```

This command searches for the word "error" in the file log.txt and prints the two lines before each match. In this example, we see the lines before the error
message, which give us a better idea of what was happening in the application just before the error occurred.

Example 7.2:

```
grep -B 3 -A 2 'error' log.txt
```

Output:

```
2023-02-25 14:03:41 - INFO - Starting application
2023-02-25 14:03:40 - INFO - Initializing database connection
2023-02-25 14:03:42 - ERROR - Failed to connect to database
2023-02-25 14:03:43 - WARNING - Retrying connection...
2023-02-25 14:03:44 - ERROR - Connection failed after 3 retries
2023-02-25 14:03:45 - INFO - Shutting down application
```

This command prints three lines before each match and two lines after each match. This gives us an even more complete picture of the context around each error
message.

Use-case:

a programmer is having trouble finding the lines of code that are causing an error. ```-B``` can be used to retreive two lines before or after each match to 
help diagnose the error properly.


Option 8: ```-f```

The -f option in grep allows you to search for patterns that are listed in a file, rather than typing them directly on the command line. This can be useful when you
have a large number of patterns to search for, or when the patterns are complex and difficult to type out manually. To use -f, you provide the name of the file
containing the patterns using the -f option followed by the name of the file. The patterns in the file should be listed one per line.

Example 8.1:

```
grep -f patterns.txt file.txt
```

Output:

```
Line 1: This is a test
Line 3: This is another test
```

This command searches for all lines in file.txt that match any of the patterns listed in patterns.txt. In this example, patterns.txt contains two patterns: "test"
and "another". The output shows the lines that match either pattern.

Example 8.2:

```
grep -v -f exclude.txt file.txt
```

Output:

```
Line 1: This is a test
Line 2: This line does not match any patterns
```

This command searches for all lines in file.txt that do not match any of the patterns

Use-case: 
A programmer is trying to find all the receipts of the company that are stored in a specific file type. ```-f``` can be used to either find that specific file type
or exclude all other file types.


Option 9: ```-s```

The -s option is used to suppress error messages that are usually displayed when a file is not found or is unreadable. The ```-s``` option can also be used in
combination with the -r option to search for a pattern recursively in a directory tree. 

Example 9.1:


```
grep -s "apple" fruits.txt
```

Output:

```
apple
pineapple
```

In this example, the command is searching for the string "apple" in the file fruits.txt. If fruits.txt does not exist, the command will not display an error message
and will simply output nothing.

Example 9.2:

```
grep -rs "apple" /usr/share/dict/
```


Output:

```
/usr/share/dict/words:apple
/usr/share/dict/words:pineapple
```

In this example, the command searches for the string "apple" in all files under the directory /usr/share/dict/. If any file cannot be read, the command will not
display an error message and will simply skip that file.

Use-case:

You can use the -s option when you want to suppress error messages that may be generated when grep searches for files that do not exist or that it cannot read.


Option 10: ```-y```

The -y option is used to ignore case sensitivity when searching for a pattern. The ```-y``` option can also be used to ignore case sensitivity when specifying a
regular expression. 


Example 10.1:

```
grep -y "test" file1.txt file2.txt
```

Output:

```
FILE1.TXT: test
FILE2.TXT: TEST
```

In this example, the command searches for the string "test" in the files file1.txt and file2.txt. Since ```-y``` is used, the search is case-insensitive, so both
"test" and "TEST" are considered matches.


Example 10.2:


```
grep -y "^[a-z]" file.txt
```


Output:

```
abc
def
```

In this example, the command searches for lines in file.txt that begin with a lowercase letter. Since -y is used, the search is case-insensitive, so lines that
begin with either uppercase or lowercase letters are considered matches.


Use-case:

You can use the -y option when you want to search for a pattern without considering the case of the characters in the pattern or the text being searched.





Source: chatGPT. ChatGPT prompt: "In what ways can I use the grep command to search through a directory"

[The Linux Documentation Project - Grep Tutorial](https://tldp.org/LDP/Bash-Beginners-Guide/html/sect_04_02.html)
