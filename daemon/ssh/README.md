## OpenSSH Server

Build a docker image for OpenSSH Server.

### Build

    docker build -t daemon/ssh .

### Usage

#### Open an SSH instance

    docker run -d -p 22:2222 -v /path/to/your/pubkey:/root/.ssh/authorized_keys daemon/ssh

and then connect with your key:

    ssh -p 2222 -i /path/to/your/private/key root@localhost
