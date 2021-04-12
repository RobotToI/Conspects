# Basic bash commands
#### cp 
    - ```-r``` рекурсивно скопирует всё из указанной директории
    - позволяет не только копировать директории, но и файлы
#### mv
    - позволяет перемещать, переименовывать, перезаписывать файлы и директории

#### mkdir
    - Позволяет создать директорию
    - параметр ```-p``` позволит нам создать директорию если её не существует, 
        если же она существует ничего не делать

#### echo 
    - поможет вам посмотреть что на самом деле введёт bash при использовании regeEX
#### rm
    - Мы можем удалять пустые директории с помощью rmdir
    - чтобы удалить непустую директорию используй ```-r``` flag

#### wc
    - Word count of file 
    - ```-l``` number of lines
    - ```-c``` number of bytes
    - ```-w``` number of words
    - ```Ctrl+D``` - say to command line that you end of file ```\0```

#### > write to file
#### >> append to file
#### < write content of file in right to command input in left like wc, cat
#### | перенаправляет вывод из левой части в stdin правой части


#### curl загружает контент из url. Лучше использовать вместе с ```-s```
#### grep фильтрует вывод
#### head prints first few characters or lines Ex.```git log|head -n1```
#### tail prints last few characters or lines
    ```-c``` characters ```-n``` lines
#### cal prints calendar with current day cal -3(prev, curr, next) *year*
#### date use +'%{HSYMD}' to print exect information that you want and print it in specific format that you want ```%F``` full date in YYYY-MM-DD
#### fold может помочь форматировать вывод в консоль если он недостаточно удобен
#### echo `data` will execute data command like echo $(date) do the same
#### export show you all your global variables
#### To define own env variables just type ```VARIABLE=VALUE```
#### quotes $VAR won't work with single quotes, but it does work with double quotes. For ex. when we do git commit -m 'our message'


# Bash scripts  
    - You don't have to put ```*.sh``` extension to your file when you create a script
### First line should be like #! /bin/bash to define that this is the bash script
    - And then you can put each command in a new line
    - To use arguments  we use $1, $2, ..., $n(positional) arguments or $*/$@ 
    (all arguments) to define an few words argument
#### While loop:
    ```bash 
        while exp; do command1; command2; done
    ```
#### For loop:
    ```bash
        for x in {0..10};do command seq; done
    ```
##### If your server allways crashs you can use ```while true; do run server; done```
#### bashrc file runs every time you run command line. you can paste to it whatever you want

### Permissions
    -user/group/other in line (-rw)*userpart*(-r--)*grouppart*(r--)*other* permissions for file of directory
    - Change permissions ```chmod ``` ugo and +/- rwx - for who you change permissions
    - ```groups``` show you what groups you are in right now.

#### There are number of exit codes 0 when have no exceptions 2 when we can't find smth and etc. (check $?)
    - while (smth exists); do smth; done pretty useful thing
    - we have the opposite of while loop sounds untill
    - && for and xD and || for or operator
    - if expressions; then ...; else ...; fi