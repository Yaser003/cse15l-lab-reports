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

Example 1.2:

```
find written_2 > find-results.txt
grep ".pdf" find-results.txt > grep-results.txt
wc grep-results.txt
```

The second command-line option I chose for this command is one I used recently in the skill demo. This command line can be used to recursively search a directory 
for files thatcontain a specified string. 

format:

```
grep -r *string*
```

Example 2.1:

grep -r Lucayans

Example 2.2

grep -r that

The third command-line option
