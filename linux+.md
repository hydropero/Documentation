
#### Linux system admin commands:

#### Adding users:

1. **useradd [OPTIONS] USERNAME**
> only root users with sudo privileges can use this command to create user accounts.
>When this command is used, it creates a new user account according to the options specified on the command line and the default values set in the **/etc/default/useradd** file.
> useradd also reads the content of the **/etc/login.defs** file. This file contains configuration for the shadow password suite such as password expiration policy, ranges of user IDs used when creating system and regular users, and more.

****
#### Parameter Expansion:

Parameter expansion is a feature in bash that allows you to manipulate variables in various ways. It's basically a way to modify or extract part of a variable's value.

Here are a few examples of how you can use parameter expansion in bash:

> **\${variable}:** This is the simplest form of parameter expansion, and it simply expands to the value of the variable. For example, if variable="Hello", 
\${variable} would expand to Hello.

> **\${variable:position:length}:** This syntax allows you to extract a substring of variable starting at position and continuing for length characters. For example, if variable="Hello, world!", 
\${variable:7:5} would expand to world.

> **\${variable#pattern}:** This syntax removes the shortest match of pattern from the beginning of variable. For example, if variable="path/to/file.txt", 
\${variable#*/} would expand to to/file.txt.

> **${variable##pattern}:** This syntax removes the longest match of pattern from the beginning of variable. For example, if variable="path/to/file.txt", 
\${variable##*/} would expand to file.txt.

> **\${variable%pattern}:** This syntax removes the shortest match of pattern from the end of variable. For example, if variable="file.txt.gz", 
\${variable%.gz} would expand to file.txt.

> **\${variable%%pattern}:** This syntax removes the longest match of pattern from the end of variable. For example, if variable="file.txt.gz", 
\${variable%%.gz} would expand to file.txt.

These are just a few examples of the many ways you can use parameter expansion in bash. It's a very powerful feature that can help you manipulate strings and variables in all sorts of ways! 