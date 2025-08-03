# Shell Variables and Expansions

This directory contains scripts that demonstrate various shell variable operations and expansions in Bash.

## Scripts Overview

### 0. `0-alias`
Creates an alias named `ls` with the value `rm *`.
- **Usage**: `source ./0-alias`
- **Effect**: After sourcing, typing `ls` will execute `rm *` instead of listing files

### 1. `1-hello_you`
Prints "hello" followed by the current Linux user.
- **Usage**: `./1-hello_you`
- **Output**: `hello username`

### 2. `2-path`
Adds `/action` to the PATH environment variable.
- **Usage**: `source ./2-path`
- **Effect**: `/action` becomes the last directory in PATH

### 3. `3-paths`
Counts the number of directories in the PATH.
- **Usage**: `source ./3-paths`
- **Output**: Number of directories in PATH

### 4. `4-global_variables`
Lists all environment variables.
- **Usage**: `source ./4-global_variables`
- **Output**: All environment variables

### 5. `5-local_variables`
Lists all local variables, environment variables, and functions.
- **Usage**: `source ./5-local_variables`
- **Output**: All variables and functions

### 6. `6-create_local_variable`
Creates a local variable named `BEST` with value `School`.
- **Usage**: `source ./6-create_local_variable`

### 7. `7-create_global_variable`
Creates a global variable named `BEST` with value `School`.
- **Usage**: `source ./7-create_global_variable`

### 8. `8-true_knowledge`
Prints the result of 128 + TRUEKNOWLEDGE environment variable.
- **Usage**: `./8-true_knowledge`
- **Prerequisites**: Set `export TRUEKNOWLEDGE=value`

### 9. `9-divide_and_rule`
Prints the result of POWER divided by DIVIDE.
- **Usage**: `./9-divide_and_rule`
- **Prerequisites**: Set `export POWER=value` and `export DIVIDE=value`

### 10. `10-love_exponent_breath`
Displays BREATH to the power of LOVE.
- **Usage**: `./10-love_exponent_breath`
- **Prerequisites**: Set `export BREATH=value` and `export LOVE=value`

### 11. `11-binary_to_decimal`
Converts a binary number stored in BINARY environment variable to decimal.
- **Usage**: `./11-binary_to_decimal`
- **Prerequisites**: Set `export BINARY=binary_number`

### 12. `12-combinations`
Prints all possible combinations of two letters, except 'oo'.
- **Usage**: `./12-combinations`
- **Output**: 675 combinations in alphabetical order

### 13. `13-print_float`
Prints a number with two decimal places.
- **Usage**: `./13-print_float`
- **Prerequisites**: Set `export NUM=number`

## Environment Variables Used

- `TRUEKNOWLEDGE`: Used in script 8
- `POWER` and `DIVIDE`: Used in script 9
- `BREATH` and `LOVE`: Used in script 10
- `BINARY`: Used in script 11
- `NUM`: Used in script 13

## Examples

```bash
# Test the alias
source ./0-alias
ls  # This will now execute 'rm *'

# Test hello script
./1-hello_you  # Output: hello username

# Test path addition
source ./2-path
echo $PATH  # /action will be at the end

# Test arithmetic with environment variables
export TRUEKNOWLEDGE=1209
./8-true_knowledge  # Output: 1337

# Test binary conversion
export BINARY=10100111001
./11-binary_to_decimal  # Output: 1337

# Test float printing
export NUM=3.14159265359
./13-print_float  # Output: 3.14
```

## Notes

- All scripts are executable
- Script 12-combinations is under 64 characters as required
- Use `source` or `.` for scripts that modify the current shell environment
- Use `./` for scripts that produce output 