# SSH

## Secure Shell

- Communication protocol. (Like http, https, ftp...)

- Connecting to remote computer.

- Traffic is encrypted. (Connection)

- SSH is the client and SSHD is the server. (Open SSH Daemon)

- The `server must have SSHD installed and running` to connect with the server.

## Encryption

- SSH uses `public key cryptography`.

- User generates a public and private key.

- Register the public key in the remote server.

- In SSH public key/private key used to authenticate users. Then Symmetric key/ Secret key will used by SSH in order to encrypt the entire connection.

- The secret key is created through a process known as a key [exchange algorithm](https://www.digitalocean.com/community/tutorials/understanding-the-ssh-encryption-and-connection-process).

## Commands

### Generating SSH Keys

> Private Key Location: `.~/.ssh/id_rsa`
> Public Key Location: `.~/.ssh/id_rsa.pub`
> Public key need to be added inside `authorized_files` which is in the server.

`$ ssh-keygen`

`$ ssh-keygen -t ed25519 -C "[mail]"`

> Flag `-t` for algorithm type.
> Flag `-C` for comment.
> Flag `-b` for number of bytes.

### Connecting to server

`$ ssh [username]@[server_ipaddress]`

### Saving SSH public key in the server

`$ ssh-copy-id [username]@[server_ipaddress]`

`$ cat ~/.ssh/id_rsa.pub | ssh [username]@[server_ipaddress] "mkdir -p ~/.ssh & chmod 700 ~/.ssh && cat >> ~/.ssh/authorized_keys"`

### Adding SSH keys generated in custom location or with custom name

`$ ssh-add ~/.ssh/[file_name]`

`$ ssh-add ~/.ssh/[folder_name]/id_rsa`

### Moving file from local machine to server

`$ scp [local_file_location] [username]@[server_ipaddress]:[server_file_location]`

## Note

- `[file_name].pub` is the public key.

- `>>` appends data to a file and `>` overwrites the file with data.

- The `$ echo $?` will returns exit status of last executed command. `true: 0, false: 1`
