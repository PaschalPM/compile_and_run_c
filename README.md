# Compile and Run C (**comrunc**)
## Description of the **comrunc** command:
As an ALX student, are you tired of having to compile your C programs everytime using this 'long command':
```bash
pasmac@ubuntumachine$: gcc -Wall -Werror -Wextra -pedantic -std=gnu89 examplefile.c
```
then having to run it afterwards to see its result?
```bash
pasmac@ubuntumachine$: ./a.out
```
> __\*\*\* USING THE "comrunc" COMMAND WILL RESOLVE THIS FOR YOU! ***__
___
## Installation of **comrunc**:
1. Clone this repository:
   ```bash
    pasmac@ubuntumachine$: git clone https://github.com/PaschalPM/compile_and_run_c.git
    ```
2.  CD into compile_and_run_c repository:
    ```bash
    pasmac@ubuntumachine$: cd compile_and_run_c
    ```
3.  Run the install script:
    ```bash
    pasmac@ubuntumachine$: sudo ./install.sh
    ```
___
## Usage of **comrunc** command:
1. ### Compile and run a single C file:
    ```bash
    pasmac@ubuntumachine$: comrunc example.c
    ```
    >***NOTE: If you do not specify a second argument, the output file will be "a.out" as usual.***

2. ### Compile and run multiple C files:
    ```bash
    pasmac@ubuntumachine$: comrunc "example1.c example2.c example3.c"
    ```
    >***NOTE: Use double quotes to hold together all C files you wish to compile.***

3. ### Compile and run a single C file **BUT** specify an output file:
    ```bash
    pasmac@ubuntumachine$: comrunc example.c outputfile
    ```
4. ### Compile and run multiple C files **BUT** specify an output file:

    ```bash
    pasmac@ubuntumachine$: comrunc "example1.c example2.c example3.c" outputfile
    ```
    >***NOTE: The specified outputfile comes after the double quotes.***

___
## More on Usage of **comrunc** command:
The **comrunc** command detects when you pass in an outputfile argument or a stage switch flag argument (Preprocessing -E, Compilation -S, Assembly -c) or both and gives the result of the specified stage regardless of how the arguments are arranged.

```bash
pasmac@ubuntumachine$: comrunc "example1.c example2.c example3.c" outputfile -E
```
OR
```bash
pasmac@ubuntumachine$: comrunc "example1.c example2.c example3.c" -E outputfile
```

>The above commands will give same result which is the Preprocessing Stage output of the compiled files. **Please NOTE, when using any of the stage switch flags, the program is not ran automatically after compilation.** 
___
## THANK YOU!!!
