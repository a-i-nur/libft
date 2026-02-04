# Libft

`libft` is the first foundational C project at 42 School.
This repository is my **first project from the 42 School Common Core Curriculum (Circle 0)**.

- Author / Intra: `aakhmeto`
- Repository: [github.com/a-i-nur/libft](https://github.com/a-i-nur/libft)

## Subject Requirements (from libft project)

| Item | Requirement |
|---|---|
| Program name | `libft.a` |
| Turn-in files | `Makefile`, `libft.h`, `ft_*.c` |
| Makefile rules | `NAME`, `all`, `clean`, `fclean`, `re`, `bonus` |
| Allowed external functions | `malloc`, `free`, `write` |
| Libft authorized | Yes |
| Goal | Recode standard libc-style utilities and add extra reusable functions |

## Project Scope

This project includes:
- reimplemented libc-like functions (string, memory, character checks, conversions)
- additional utility functions required by the subject
- bonus linked-list API (`t_list`)

Current scope in this repository:
- `23` libc-style reimplemented functions
- `11` libft-specific functions
- `9` bonus linked-list functions

## Build

```bash
make        # mandatory part
make bonus  # mandatory + linked-list bonus
make clean
make fclean
make re
```

The build output is a static library: `libft.a`.

## 1) Libc-Style Functions

| Function | Description | Original library |
|---|---|---|
| [`ft_isalpha`](https://github.com/a-i-nur/libft/blob/main/ft_isalpha.c) | Check whether a character is alphabetic. | `isalpha` (`<ctype.h>`) |
| [`ft_isdigit`](https://github.com/a-i-nur/libft/blob/main/ft_isdigit.c) | Check whether a character is a digit. | `isdigit` (`<ctype.h>`) |
| [`ft_isalnum`](https://github.com/a-i-nur/libft/blob/main/ft_isalnum.c) | Check whether a character is alphanumeric. | `isalnum` (`<ctype.h>`) |
| [`ft_isascii`](https://github.com/a-i-nur/libft/blob/main/ft_isascii.c) | Check whether value is in ASCII range. | `isascii` (`<ctype.h>`, extension) |
| [`ft_isprint`](https://github.com/a-i-nur/libft/blob/main/ft_isprint.c) | Check whether a character is printable. | `isprint` (`<ctype.h>`) |
| [`ft_strlen`](https://github.com/a-i-nur/libft/blob/main/ft_strlen.c) | Return string length. | `strlen` (`<string.h>`) |
| [`ft_memset`](https://github.com/a-i-nur/libft/blob/main/ft_memset.c) | Fill memory with a byte value. | `memset` (`<string.h>`) |
| [`ft_bzero`](https://github.com/a-i-nur/libft/blob/main/ft_bzero.c) | Zero out a memory block. | `bzero` (`<strings.h>`, legacy) |
| [`ft_memcpy`](https://github.com/a-i-nur/libft/blob/main/ft_memcpy.c) | Copy memory (no overlap support). | `memcpy` (`<string.h>`) |
| [`ft_memmove`](https://github.com/a-i-nur/libft/blob/main/ft_memmove.c) | Copy memory (overlap-safe). | `memmove` (`<string.h>`) |
| [`ft_strlcpy`](https://github.com/a-i-nur/libft/blob/main/ft_strlcpy.c) | Size-bounded string copy. | `strlcpy` (BSD libc) |
| [`ft_strlcat`](https://github.com/a-i-nur/libft/blob/main/ft_strlcat.c) | Size-bounded string concatenation. | `strlcat` (BSD libc) |
| [`ft_toupper`](https://github.com/a-i-nur/libft/blob/main/ft_toupper.c) | Convert character to uppercase. | `toupper` (`<ctype.h>`) |
| [`ft_tolower`](https://github.com/a-i-nur/libft/blob/main/ft_tolower.c) | Convert character to lowercase. | `tolower` (`<ctype.h>`) |
| [`ft_strchr`](https://github.com/a-i-nur/libft/blob/main/ft_strchr.c) | Find first occurrence of a character in a string. | `strchr` (`<string.h>`) |
| [`ft_strrchr`](https://github.com/a-i-nur/libft/blob/main/ft_strrchr.c) | Find last occurrence of a character in a string. | `strrchr` (`<string.h>`) |
| [`ft_strncmp`](https://github.com/a-i-nur/libft/blob/main/ft_strncmp.c) | Compare two strings up to `n` chars. | `strncmp` (`<string.h>`) |
| [`ft_memchr`](https://github.com/a-i-nur/libft/blob/main/ft_memchr.c) | Find a byte in memory. | `memchr` (`<string.h>`) |
| [`ft_memcmp`](https://github.com/a-i-nur/libft/blob/main/ft_memcmp.c) | Compare two memory areas. | `memcmp` (`<string.h>`) |
| [`ft_strnstr`](https://github.com/a-i-nur/libft/blob/main/ft_strnstr.c) | Find substring within size limit. | `strnstr` (BSD libc) |
| [`ft_atoi`](https://github.com/a-i-nur/libft/blob/main/ft_atoi.c) | Convert string to `int`. | `atoi` (`<stdlib.h>`) |
| [`ft_calloc`](https://github.com/a-i-nur/libft/blob/main/ft_calloc.c) | Allocate and zero-initialize memory. | `calloc` (`<stdlib.h>`) |
| [`ft_strdup`](https://github.com/a-i-nur/libft/blob/main/ft_strdup.c) | Duplicate a string into new memory. | `strdup` (POSIX) |

## 2) Libft-Specific Functions

| Function | Description | Original library |
|---|---|---|
| [`ft_substr`](https://github.com/a-i-nur/libft/blob/main/ft_substr.c) | Extract a substring by start index and length. | No direct libc equivalent |
| [`ft_strjoin`](https://github.com/a-i-nur/libft/blob/main/ft_strjoin.c) | Join two strings into a new one. | No direct libc equivalent |
| [`ft_strtrim`](https://github.com/a-i-nur/libft/blob/main/ft_strtrim.c) | Trim a set of characters from both string ends. | No direct libc equivalent |
| [`ft_split`](https://github.com/a-i-nur/libft/blob/main/ft_split.c) | Split a string by delimiter into string array. | No direct libc equivalent |
| [`ft_itoa`](https://github.com/a-i-nur/libft/blob/main/ft_itoa.c) | Convert `int` to string. | No direct libc equivalent |
| [`ft_strmapi`](https://github.com/a-i-nur/libft/blob/main/ft_strmapi.c) | Build new string by applying function to each char. | No direct libc equivalent |
| [`ft_striteri`](https://github.com/a-i-nur/libft/blob/main/ft_striteri.c) | Apply function in-place to each char. | No direct libc equivalent |
| [`ft_putchar_fd`](https://github.com/a-i-nur/libft/blob/main/ft_putchar_fd.c) | Write one character to file descriptor. | No direct libc equivalent |
| [`ft_putstr_fd`](https://github.com/a-i-nur/libft/blob/main/ft_putstr_fd.c) | Write string to file descriptor. | No direct libc equivalent |
| [`ft_putendl_fd`](https://github.com/a-i-nur/libft/blob/main/ft_putendl_fd.c) | Write string + newline to file descriptor. | No direct libc equivalent |
| [`ft_putnbr_fd`](https://github.com/a-i-nur/libft/blob/main/ft_putnbr_fd.c) | Write integer to file descriptor. | No direct libc equivalent |

## 3) Bonus Functions (Linked List)

| Function | Description | Original library |
|---|---|---|
| [`ft_lstnew`](https://github.com/a-i-nur/libft/blob/main/ft_lstnew.c) | Create a new list node (`t_list`). | No direct libc equivalent |
| [`ft_lstadd_front`](https://github.com/a-i-nur/libft/blob/main/ft_lstadd_front.c) | Add node to beginning of list. | No direct libc equivalent |
| [`ft_lstsize`](https://github.com/a-i-nur/libft/blob/main/ft_lstsize.c) | Count nodes in list. | No direct libc equivalent |
| [`ft_lstlast`](https://github.com/a-i-nur/libft/blob/main/ft_lstlast.c) | Get last node of list. | No direct libc equivalent |
| [`ft_lstadd_back`](https://github.com/a-i-nur/libft/blob/main/ft_lstadd_back.c) | Add node to end of list. | No direct libc equivalent |
| [`ft_lstdelone`](https://github.com/a-i-nur/libft/blob/main/ft_lstdelone.c) | Delete one node using `del` callback. | No direct libc equivalent |
| [`ft_lstclear`](https://github.com/a-i-nur/libft/blob/main/ft_lstclear.c) | Delete and clear entire list. | No direct libc equivalent |
| [`ft_lstiter`](https://github.com/a-i-nur/libft/blob/main/ft_lstiter.c) | Iterate over list and apply function to content. | No direct libc equivalent |
| [`ft_lstmap`](https://github.com/a-i-nur/libft/blob/main/ft_lstmap.c) | Map list into new list with transform function. | No direct libc equivalent |

## Project Structure

- Header: [`libft.h`](https://github.com/a-i-nur/libft/blob/main/libft.h)
- Build system: [`Makefile`](https://github.com/a-i-nur/libft/blob/main/Makefile)
- Output library: `libft.a`

## Skills Developed in This Project

This project develops practical low-level C skills:
- memory management (`malloc`, `free`) and pointer safety
- robust handling of edge cases in string and memory operations
- writing reusable APIs and organizing code into a static library
- working with a C header (`libft.h`): prototypes, types, and interface contracts
- working with `Makefile` rules (`all`, `clean`, `fclean`, `re`, `bonus`) and static archive generation
- implementing and using a custom singly linked list API (`t_list`) with creation, traversal, mapping, and cleanup

## Key Achievements

- Built a reusable static C library (`libft.a`) from scratch with consistent API design.
- Implemented `43` core utility functions covering strings, memory, conversion, output, and linked lists.
- Structured the project with clear separation of interface (`libft.h`), implementation (`ft_*.c`), and build pipeline (`Makefile`).
- Completed both mandatory and bonus scopes, including a full singly linked list module.

## How This Maps to Real-World Engineering

- **Code reliability:** careful edge-case handling and defensive memory usage translate directly to production C/C++ code.
- **Maintainability:** header-driven interfaces and modular source files mirror real library and service architecture.
- **Build discipline:** Makefile targets and static library packaging reflect CI/CD and reproducible build practices.
- **Data structure fluency:** linked list operations build a foundation for more advanced algorithmic and systems tasks.
