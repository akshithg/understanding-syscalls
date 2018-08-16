# 𝚎𝚡𝚎𝚌𝚟𝚎()

`int execve(const char *filename, char *const argv[], char *const envp[]);`

`filename`: the program to execute

`argv`: NULL-terminated list of command line arguments

`envp`: NULL-terminated list of environment variables

---
``` sh
$ make

$ ./do_execve # run without any arguments
Failed to execute '(null)', Bad address

$ ./do_execve 1 2 3 # pass random arguments
Failed to execute '1', No such file or directory

$ ./do_execve show_info # pass an executable
argv[0] = 'zero'
argv[1] = 'one'
argv[2] = 'two'
ENVVAR1=1
ENVVAR2=2

$ ./do_execve show_info.sh # pass a shell script
$0 = 'show_info.sh'
$1 = 'one'
$2 = 'two'
ENVVAR1=1
ENVVAR2=2
PWD=/home/akshithg/workspace/understanding-syscalls/execve
```
