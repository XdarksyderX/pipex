
# Pipex

## Overview
`pipex` is a project that mimics the behavior of shell pipelines in Unix systems. It demonstrates the use of pipes, file descriptors, and process creation and management using the `fork`, `exec`, and `pipe` system calls in C. This project is part of a deep dive into UNIX mechanisms and processes, typically undertaken by students at 42 school.

## Features
- Implementation of Unix pipe mechanisms in C.
- Execution of commands and handling of input/output redirections.
- Bonus part: Handling multiple pipes, allowing the chaining of multiple commands, similar to using multiple pipes in a shell.

## Compilation and Usage
### Requirements
- GCC compiler
- GNU make

### Compiling the Program
To compile `pipex`, run:

```
make all
```

This command compiles the `pipex` executable, which can be used to execute commands in a pipeline fashion.

### Compiling the Bonus Program
For the bonus part, which includes the functionality to handle multiple pipes:

```
make bonus
```

### Cleaning Up
To remove all compiled files:

```
make fclean
```

To recompile:

```
make re
```

## File Structure
- `src/*.c` - Source files for the main pipex functionalities.
- `src/bonus/*.c` - Additional features for handling multiple pipes in the bonus part.

## Usage
To use `pipex`, provide it with input and output files and the commands you want to execute, like so:

```
./pipex infile "command1" "command2" outfile
```

For the bonus part with multiple pipes:

```
./pipex infile "command1" "command2" "command3" ... "commandN" outfile
```

This will execute the commands in a chained fashion, passing the output of one command as the input to the next, and writing the final output to `outfile`.
