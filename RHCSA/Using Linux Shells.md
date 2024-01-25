[Table of Contents](/RHCSA/RHCSA%20Table%20of%20Contents.md)

# Viewing and Comparing File Contents from a Shell
* `cat` - prints file contents
* `tac` - prints file contents but in reverse
* `more` - page-by-page file contents
* `less` - allows content viewing with ability to scroll
* `diff $FILE1 $FILE2` - shows the difference between `$FILE1` and `$FILE2`

# Create Aliases and Links
## Alias
Saves time by assigning an alias that refers to a longer version of a command.
Example: `alias ipadd='<very long complex command>'`
To make this permanent, add alias to `bash.profile`
## Links
* `ln source_file link_name` - creates a link that points to a file
* inode - metadata of a file; the way Linux keeps track of files
* **Hard links** does not create new inodes. It's another file that points to the same inode the *original file* was in. You can delete the original file and the hard links is still valid.
* **Soft links** creates a new inode. This can create a link that points to the file with a different owner and permissions.

# Customize the Bourne Again Shell
* `$PS1` shows how the prompt looks like
* Most variables in Linux are uppercase.
* `export` lets the variable be exported so it can be available outside the current shell's scope.
* `setenv` creates environment variables.

# Creating and Editing Files in the Shell

Next: [File Management](File%20Management.md)