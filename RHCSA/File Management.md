[Table of Contents](/README.md)

# Filename Globbing
## Filename Globbing
Allows file selection using a pattern match. Look for consistency in filenames.
Example:
* `ls *2014*` returns filenames with 2014 in their name.
* `ls *201[34]*` returns filenames with either 2013 or 2014.
* `ls [East,West]*` returns files that start with either East or West in one command
* `ls *{2013..2015}` shows files that end with 2013, 2014 and 2015 
* You can compare more regular expressions in one command.

# Performing Searches for Files
* `find` searches for files recursively.
* `find -name "Project*"` returns files that are found.
* `find . -type f -print | wc -l`
* `find -user $USER` finds files owned by $USER

# Performing Actions on Files that are Found