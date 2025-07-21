# C Piscine C03

![42 Badge](https://img.shields.io/badge/42-C_Piscine-orange)
![C Badge](https://img.shields.io/badge/Language-C-blue)
![Status Badge](https://img.shields.io/badge/Status-Completed-success)

## What I Learned

Through this C03 module of the 42 School C Piscine, I developed essential string manipulation and comparison skills:

- **String comparison algorithms** - Implemented character-by-character comparison logic for both bounded and unbounded strings
- **Memory-safe string operations** - Learned to handle string concatenation with proper buffer management and overflow prevention
- **Pointer arithmetic mastery** - Advanced understanding of pointer manipulation for efficient string traversal and modification
- **Pattern matching algorithms** - Implemented substring search functionality using efficient string searching techniques
- **Buffer management** - Gained expertise in size-limited operations to prevent buffer overflows and memory corruption
- **Edge case handling** - Developed robust functions that handle NULL pointers, empty strings, and boundary conditions
- **Performance optimization** - Balanced code readability with efficient memory access patterns
- **Standard library understanding** - Deep comprehension of how fundamental C library functions work internally
- **Defensive programming** - Added comprehensive input validation and error prevention mechanisms
- **Code maintainability** - Wrote clean, well-structured functions following 42's strict coding standards (Norminette)

This project strengthened my low-level programming skills and understanding of how string operations work at the memory level, essential knowledge for any systems programming role.

## About the Project

C03 is a crucial module in the 42 School C Piscine that focuses on string manipulation and comparison functions. Students must reimplement fundamental C standard library functions to understand their inner workings and develop proficiency in:

- String comparison and analysis
- Safe string concatenation
- Substring searching and pattern matching
- Memory-bounded string operations
- Pointer manipulation for string processing

## Implementation Details

The project consists of 6 exercises, each implementing a core string manipulation function:

### String Comparison Functions

| Function | Purpose | Key Challenge |
|----------|---------|---------------|
| **ft_strcmp** | Compare two strings lexicographically | Implementing proper ASCII value comparison and handling string termination |
| **ft_strncmp** | Compare first n characters of strings | Adding boundary checking while maintaining comparison accuracy |

### String Concatenation Functions

| Function | Purpose | Key Challenge |
|----------|---------|---------------|
| **ft_strcat** | Concatenate source string to destination | Managing destination buffer and proper null termination |
| **ft_strncat** | Concatenate up to n characters | Combining length limits with safe concatenation practices |
| **ft_strlcat** | Size-bounded string concatenation | Preventing buffer overflows while returning useful length information |

### String Search Functions

| Function | Purpose | Key Challenge |
|----------|---------|---------------|
| **ft_strstr** | Find substring within a string | Implementing efficient pattern matching without built-in functions |

## Function Prototypes

```c
// String comparison
int ft_strcmp(char *s1, char *s2);
int ft_strncmp(char *s1, char *s2, unsigned int n);

// String concatenation
char *ft_strcat(char *dest, char *src);
char *ft_strncat(char *dest, char *src, unsigned int nb);
unsigned int ft_strlcat(char *dest, char *src, unsigned int size);

// String search
char *ft_strstr(char *str, char *to_find);
```

## Usage

```bash
# Compile individual exercises
cc -Wall -Wextra -Werror ft_strcmp.c main.c -o test_strcmp

# Test with custom main function
./test_strcmp
```

## Example Usage

```c
#include <stdio.h>

// Example usage of implemented functions
int main(void)
{
    char dest[50] = "Hello ";
    char src[] = "World!";
    char *result;
    int cmp_result;
    
    // String comparison
    cmp_result = ft_strcmp("abc", "abc");  // Returns 0
    cmp_result = ft_strncmp("abcd", "abxy", 2);  // Returns 0 (first 2 chars match)
    
    // String concatenation
    ft_strcat(dest, src);  // dest becomes "Hello World!"
    
    // Substring search
    result = ft_strstr("Hello World!", "World");  // Points to "World!"
    
    return (0);
}
```

## Technical Challenges Overcome

- **Null pointer handling** - Ensuring functions behave correctly with NULL inputs without segmentation faults
- **Buffer overflow prevention** - Implementing size-bounded operations that respect destination buffer limits
- **Efficient string traversal** - Optimizing pointer arithmetic for minimal memory access overhead
- **Pattern matching optimization** - Creating substring search that efficiently handles various edge cases
- **Memory boundary respect** - Understanding when to stop operations based on string terminators vs size limits
- **Standard compliance** - Matching exact behavior of standard library functions including return values and side effects

## Project Requirements

- **Compilation flags**: `-Wall -Wextra -Werror`
- **Forbidden functions**: All standard library string functions
- **Norminette compliance**: All code must pass 42's strict coding standard checker
- **No memory leaks**: Proper memory management throughout all implementations
- **Edge case handling**: Functions must handle empty strings, NULL pointers, and boundary conditions

## Historical Context

The project includes an interesting foreword about the history of Rock-Paper-Scissors, tracing its origins from ancient China through its evolution in Japan and eventual spread to the Western world. This cultural context emphasizes the global nature of problem-solving patterns - much like how string manipulation techniques are fundamental across all programming languages and cultures.

---

*This project was completed as part of the 42 School C Piscine, demonstrating proficiency in low-level C programming, algorithm implementation, and systems-level understanding of string operations.*

---


## License

This project is licensed under the [MIT License](./LICENSE).
