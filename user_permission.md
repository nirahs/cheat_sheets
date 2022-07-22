# Changing the permission for folders and files

## Notes

- Commands `chmod` and `chown` is used to change folders and files permission.

- There are three types of users who can interact with a file. Those are `Owner`, `Group`, `Others`.

- Owner: The user who creates and owns a file or folder.

- Group: All users who are members of the same group.

- Others: All the other users on the system who are neither the owner nor members of a group.

- Command `$ ls -l` to see the files and folders permissions. This command will return `drwxrwxr-x  3 [username] [username] 4096 Sep 14 03:53 .vscode`.

- The word `drwxrwxr-x` represents permissions. This word have to divided into four groups `d` , `rwx` , `rwx` , `r-x`. Here

  - `d` : directory

  - `r` : read : 4

  - `w` : write : 2

  - `x` : execute : 1

- The above numbers (4, 2, 1) determines the file permissions. Read, write, execute are represented by numerical value.

- If it's a file first group will be `-`. If a user doesn't have specific permission then it will be replaced with `-`. For example if a user/group/others doesn't have permission to execute but the user/group/others can read and write, then permission line will be `rw-`.

- In the four group, first group indicates the file type if it's a file it will be `-`. The second group indicates the owner's permission. The third group indicates group's permissions. The last group permission indicates other's permissions.

- The number will represents number of hard links. Hard link means in short additional name for an existing file. Further more: [Hard Link in Linux](https://linuxhandbook.com/hard-link/)

- Then next two word represents `owner` and `group owner`.

- Then the data represents last modfied data.

- Then last word represents the file or file_name.

## Using chmod

### Changing permission

`chmod 744 [file_name]`

> The above command will give owner read, write, execute permission and for other users this command will only give read permission.

> 7 (owner) = 4 (read) + 2 (write) + 1 (execute).

> 4 (group owner) = 4 (read)

> 4 (other) = 4 (read)

## Using chown

### Chaning owner

`$ chown [owner] [file_name]`

### Changing group owner

`$ chown :[group owner] [file_name]`

### Changing owner and group owner

`$ chown [owner]:[group owner] [file_name]`

## Flags

> Recursive flag. Recursivly change file permission in specific folders

`$ chown -R 755 [file_name]`

> Force flag. Force any errors and apply the change. Here chaing the permission.

`$ chown -f 755 [file_name]`

> Verbose flag. Give diagnositics of all files that are processed by the command.

`$ chown -v 755 [file_name]`

> Change flag. Give diagnositics only if the changes were successfully made.

`$ chown -c 755 [file_name]`
