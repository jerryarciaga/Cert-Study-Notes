# Authentication and Authorization
* Authentication: proof of identity (`/etc/passwd` file)
* Authorization: specific access
## Authentication
* Username/password
* key fobs
* Azure Active Directory (AD) authentication
### Linux Pluggable Authentication Modules (PAM)
* Separates authentication tasks from applications
* Normally configured indirectly when used with SSH

# Pluggable Authentication Modules (PAM)
PAMs separates authentication and application tasks and application tasks.
## PAM configuration
* Most Linux admins do not modify PAM directly
* Linux commands change PAM configs
## PAM Library files
* found under `/lib/*/modules`
* `/etc/pam.d` contains config files for PAM
## Syntax
* From **left** to **right**
	* Module type such as account.
	* Control-flag: such as **required**
	* Module filename, such as pam_nologin.so
* Example: `account required pam_nologin.so`
### Example: SSH Denied Users using `/etc/pam.d/sshd`
```
auth required pam_listfile.so onerr=succeed \
item=user sense=deny file=/etc/ssh/deniedusers
```

# Manage Linux User Accounts and Password Settings
`/etc/passwd` returns users, user ID and group ID
`/etc/shadow` returns password hashes
`/etc/group` returns list of groups and group IDs

# Using `sudo` to Gain Elevated Privileges
Example: In `/etc/sudoers`:
```
root ALL=(ALL:ALL) ALL
<user> <host>=(<target run-as user>:<target run-as group>) <which command>
```