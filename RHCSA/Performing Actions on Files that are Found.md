[Table of Contents](/README.md)

* `find -user cblackwell -name "Project[0-9][0-9].txt"* -exec ls -l {} \;` 
* The command above finds files that match the statements specified in `-user` and `-name`. Here, `-exec` executes the command specified, `ls -l` and `{}` acts as a placeholder.
* It usually is terminated with an escaped semicolon `\;`

Previous: [File Management](/RHCSA/File%20Management.md)