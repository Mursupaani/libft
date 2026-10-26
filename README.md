# Libft

## Description
Libft is a custom C library that replicates the behavior of standard C library (libc) functions, along with additional utility functions for string manipulation, memory allocation, and file descriptor output.

## Instructions

### Compilation
The library is compiled using the provided `Makefile`. It uses `cc` with the flags `-Wall -Wextra -Werror`.

*   **`make`**: Compiles the mandatory part and generates the `libft.a` static library.
*   **`make bonus`**: Compiles the mandatory and bonus parts (linked list functions) and adds them to `libft.a`.
*   **`make clean`**: Removes all object (`.o`) files.
*   **`make fclean`**: Removes all object files and the `libft.a` file.
*   **`make re`**: Performs a full recompilation (`fclean` followed by `make`).

### Usage
To use the library in your projects:
1. Include the header in your C files:
   ```c
   #include "libft.h"
   ```
2. Compile your project with the library:
   ```bash
   cc your_file.c -L. -lft -o your_program
   ```

## Library Details

### Part 1 - Libc Functions
Standard C library functions rebuilt from scratch:
*   **Character checking:** `ft_isalpha`, `ft_isdigit`, `ft_isalnum`, `ft_isascii`, `ft_isprint`
*   **Character manipulation:** `ft_toupper`, `ft_tolower`
*   **String manipulation:** `ft_strlen`, `ft_strchr`, `ft_strrchr`, `ft_strncmp`, `ft_strnstr`, `ft_strlcpy`, `ft_strlcat`
*   **Memory manipulation:** `ft_memset`, `ft_bzero`, `ft_memcpy`, `ft_memmove`, `ft_memchr`, `ft_memcmp`
*   **Conversion and Allocation:** `ft_atoi`, `ft_calloc`, `ft_strdup`

### Part 2 - Additional Functions
Utility functions for string and memory handling:
*   `ft_substr` - Extracts a substring from a string.
*   `ft_strjoin` - Concatenates two strings into a new string.
*   `ft_strtrim` - Trims specified characters from the beginning and end of a string.
*   `ft_split` - Splits a string into an array of words using a delimiter.
*   `ft_itoa` - Converts an integer to a string.
*   `ft_strmapi` - Applies a function to each character of a string, creating a new string.
*   `ft_striteri` - Applies a function to each character of a string by address.
*   `ft_putchar_fd` - Outputs a character to a given file descriptor.
*   `ft_putstr_fd` - Outputs a string to a given file descriptor.
*   `ft_putendl_fd` - Outputs a string to a given file descriptor, followed by a newline.
*   `ft_putnbr_fd` - Outputs an integer to a given file descriptor.

### Part 3 - Bonus Functions (Linked Lists)
Functions to manipulate the `t_list` structure:
*   `ft_lstnew` - Creates a new list node.
*   `ft_lstadd_front` - Adds a node to the beginning of the list.
*   `ft_lstsize` - Counts the number of nodes in a list.
*   `ft_lstlast` - Returns the last node of a list.
*   `ft_lstadd_back` - Adds a node to the end of a list.
*   `ft_lstdelone` - Frees the memory of a node's content and the node itself.
*   `ft_lstclear` - Deletes and frees a node and all its successors.
*   `ft_lstiter` - Applies a function to the content of all nodes in a list.
*   `ft_lstmap` - Applies a function to each node's content and creates a new list from the results.
