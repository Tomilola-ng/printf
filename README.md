# printf

### Description

---

The printf function sends formatted output to stdout.
A custom \_printf() for learning purposes was developed by cohort #9 students Jimmer and Edward Ortiz.
\_printf() function format string is a character string, beginning and ending in its initial shift state, if any.
These arguments are placed using the percentage '%' operator

---

#### Resources

---

Secrets of printfby Don colton
https://www.cypress.com/file/54761/download

---

#### Authorized functions and macros

---

write (man 2 write)
malloc (man 3 malloc)
free (man 3 free)
va_start (man 3 va_start)
va_end (man 3 va_end)
va_copy (man 3 va_copy)
va_arg (man 3 va_arg)

---

#### Compilation

---

The code must be compiled this way:

**$ gcc -Wall -Werror -Wextra -pedantic \*.c**

As a consequence, be careful not to push any c file containing a main function in the root directory of your project (you could have a test folder containing all your tests files including main functions)

The main files will include your main header file (holberton.h): **#include holberton.h**

---

#### Use & Examples

---

**Prototype:** int \_printf(const char \*format, ...);
**Use - General:** \_printf("format string", var1, var2, ...);

**Examples:**

- Basic String: \_printf("%s Holberton", "Hello");`

  - Output: Hello Holberton

- Print integers: \_printf("This is an array element: arr[%d]:%c", 32, arr[32]);`
  - Output: This is an array element arr[32]:A

Many other specifiers and flags were added and by combinig those the \_printf() function generate a different ouput. The following list are the specifiers and flags allowed.

---

#### Use & Examples

---

###### Specifiers

| Specifier  | Output                                              | Examples        |
| ---------- | --------------------------------------------------- | --------------- |
| `c`        | Character                                           | y               |
| `d` or `i` | Signed integer                                      | 1024, -1024     |
| `s`        | String of characters                                | Hello Holberton |
| `b`        | Binary Representation of unsigned integer           | 01010110        |
| `u`        | Unsigned integer                                    | 1024            |
| `o`        | Unsigned octal                                      | 432             |
| `x`        | Unsigned hexadecimal integer                        | 3ca             |
| `X`        | Unsigned hexadecimal integer (uppercase)            | 3CA             |
| `S`        | String with hex-ascii value replacing special chars | \x0A\x0A        |
| `p`        | Pointer address                                     | 0x403212        |
| `r`        | Reversed string of characters                       | dlroW olleH     |
| `R`        | ROT13 Translation of string                         | Uryyb           |

###### Flags (In development...)

| Flag      | Description                                                                                                                                           |
| --------- | ----------------------------------------------------------------------------------------------------------------------------------------------------- |
| `-`       | Left-justify the output within the field width that was given; Right justification is the default (see _width_ sub-specifier).                        |
| `+`       | Preceeds the result with a plus or minus sign (`+` or `-`) even for positive numbers. By default, only negative numbers are preceded with a `-` sign. |
| `(space)` | If no sign is going to be written, a blank space is inserted before the value.                                                                        |
| `#`       | Used with `o`, `x` or `X` specifiers the value is preceeded with 0, 0x or 0X respectively for values different than zero.                             |
| `0`       | Left-pads the number with zeroes (`0`) instead of spaces when padding is specified (see _width_ sub-specifier).                                       |

###### Width (In development...)

| Width      | Description                                                                                                                                                                                          |
| ---------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `(number)` | Minimum number of characters to be printed. If the value to be printed is shorter than this number, the result is padded with blank spaces. The value is not truncated even if the result is larger. |
| `*`        | The _width_ is not specified in the _format_ string, but as an additional integer value argument preceding the argument that has to be formatted.                                                    |

### Precision (In development...)

| .Precision  | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| ----------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `.(number)` | **For integer specifiers (`d`, `i`, `o`, `u`, `x`, `X`):** _precision_ specifies the minimum number of digits to be written. If the value to be written is shorter than this number, the result is padded with leading zeros. The value is not truncated even if the result is longer. A _precision_ of 0 means that no character is written for the value 0. **For `s`**: this is the maximum number of characters to be printed. By default all characters are printed until the ending null character is encountered. If the period is specified without an explicit value for _precision_, 0 is assumed. |

### Lenght modifiers (In development...)

| Modifier/Specifier | `d` & `i` | `u`, `o`, `x`, `X` | `c` | `s`          | `p`          |
| ------------------ | --------- | ------------------ | --- | ------------ | ------------ |
| `none`             | int       | unsigned int       | int | char pointer | void pointer |
| `h`                | short int | unsigned short int |     |              |              |
| `l`                | long int  | unsigned long int  |     |              |              |

---


- [Muiz Oyebowale](https://github.com/muizzyranking)
- [Oluwafemi Tomilola](https://github.com/Tomilola-ng)
