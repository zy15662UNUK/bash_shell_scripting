### shell and environmental path
set the environmental path
```
export env hello="world" #change and export the change to the current terminal
```
run
```
echo $hello
```

unset the environmental path

```
env -u hello #remove from the env
unset hello #clear form the export
```

### common commands
```
ls -ail # -i is to see the inode with address
ls -lrt # -t show the time, -r show the time in reverse order
cat > abc.txt # create a abc.txt and start typeing into it

rmdir test/ # rm the dir, like rm -rf
history # get command history. can be deleted from the /home/jiahao/.bash_history

```

### vim command
to enter command mode: `esc` 

to delete a line: `dd` 　

delete 3 characters : `esc 3dw`

delete current one char : `x`

copy one line: `yank yy`

to insert insert mode: `i`

### find command
find all files under certain path: `find <pathname>`

find certain file under certain path: `find <pathname> -name <filename>`

find certain file under certain path case insensitive: `find <pathname> -iname <filename>`

find reg match file under certain path case insensitive: `find <pathname> -iname "*.cpp"`

find reg match file under certain path case insensitive and with maximum recursive depth: `find <pathname> -maxdepth 2 -iname "*.cpp"`

find file under that is not xxx  certain path case insensitive and with maximum recursive depth: `find <pathname> -not -iname "xxx`

find all .cpp files or .h files: `find . -iname "*.cpp" -o -iname "*.h"`

find all .cpp files and with key word thread: `find . -iname "*.cpp" -a -iname "*thread*"`

find all files with name "abc" and are not php files: `find . -iname "abc*" ! -iname "*.php"`

find all regular files start with name "abc": `find . -type f -iname "abc*"`

find all dirtary files start with name "abc": `find . -type d -iname "abc*"`

find all regular files start with name "abc" in 2 directories: `find <pathname1> <pathname2> -type d -iname "abc*"`

find all regular files whose permission is not 777: `find . -type d ! -perm 777`

find all regular files who has read permission: `sudo find / -perm /u=r`

find all files who belongs to user john: `sudo find /home -user john`

find all files who was accessed in 10 days: `sudo find / -atime 10`

find files and exec command: `sudo find . -exec ls -ld {} \;`  or  `find . -iname "*.cpp" | xargs ls -l {} \;` xargs pipe the result of first part to the second command