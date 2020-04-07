# Bash scripting #

<!-- vscode-markdown-toc -->
* [Script file ##](#Scriptfile)
* [Interpreter ##](#Interpreter)
  * [Interpreter Options ###](#InterpreterOptions)
* [Special Characters ##](#SpecialCharacters)
* [Variables ##](#Variables)
  * [Arrays ###](#Arrays)
* [References](#References)

<!-- vscode-markdown-toc-config
	numbering=false
	autoSave=true
	/vscode-markdown-toc-config -->
<!-- /vscode-markdown-toc -->

## <a name='Scriptfile'></a>Script file ##

* Provide a meaningful short name for the script, preferably one word.
* Use `.sh` extension for the file during development to enable extension based features in modern editors.  Before release, remove the `.sh` extension if possible as it looks like a command.
* Ensure script file has executable permission set for proper user/group using `chmod` and `chown`.

## <a name='Interpreter'></a>Interpreter ##

* Use `#!/usr/bin/env bash` as interpreter. [1]
* Has to be the first line of the script
* Shebang is a 2 byte magic number that designates a executable shell script ( see `man magic` and `man file`). [2]
* Interpreter should exist at the specified path; if not, `Command not found` error would be reported.

### <a name='InterpreterOptions'></a>Interpreter Options ###

> TODO - cover options like xtrace, pipefail etc.

## <a name='SpecialCharacters'></a>Special Characters ##

* `#` - Comment lines. Can come after a command i.e. `echo "hello"   # will echo` is valid comment.
* `;` - Command separator. Helps write two commands on same line. `cd /tmp; touch t1`
* `;;` - Case option block terminator.
* `.` - has multiple contextual meanings. As a command it is used to source a file. Leading dot in filename makes the file hidden. For directoy, single dot means current directory and two dots mean parent directory.



## <a name='Variables'></a>Variables ##

> TODO - cover declare, variable attributes , local global
> read this https://stackoverflow.com/questions/45409822/bash-local-and-readonly-variable

### <a name='Arrays'></a>Arrays ###

- Variables can be Indexed or Associative arrays
- **Indexed**: normal array with numeric index starting at 0
  - Create: `mapfile -t array_name < <(ls | tail -n+2 | rev | cut -d " " -f 1 |rev)`
- **Associative**: like a map or a dictionary, index is a key instead of a numeric integer
  ```
  ```
  - Create: `mapfile -t array_name < <(ls | tail -n+2 | rev | cut -d " " -f 1 |rev)`
```bash
```









## <a name='References'></a>References

1. [Make Linux/Unix Script Portable With #!/usr/bin/env As a Shebangy][1]
1. [The shebang magic][2]


[1]: https://www.cyberciti.biz/tips/finding-bash-perl-python-portably-using-env.html
[2]: https://www.tldp.org/LDP/abs/html/abs-guide.html#MAGNUMREF