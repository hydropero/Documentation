
#### Linux system admin commands:

#### Adding users:

1. **useradd [OPTIONS] USERNAME**
> only root users with sudo privileges can use this command to create user accounts.
>When this command is used, it creates a new user account according to the options specified on the command line and the default values set in the **/etc/default/useradd** file.
> useradd also reads the content of the **/etc/login.defs** file. This file contains configuration for the shadow password suite such as password expiration policy, ranges of user IDs used when creating system and regular users, and more.

****
