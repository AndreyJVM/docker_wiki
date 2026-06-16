### Install LXC and LXD in Linux (Debian)

```shell
sudo apt update && sudo apt install lxc lxd-installer
```

### Init default settings
```shell
lxd init
# Answer the questions
```

### Run first container
```shell
lxc launch ubuntu:24.04 my-web-container -p default
```

```shell
lxc list
```

```shell
+------------------+---------+----------------------+------+-----------+-----------+
|       NAME       |  STATE  |         IPV4         | IPV6 |   TYPE    | SNAPSHOTS |
+------------------+---------+----------------------+------+-----------+-----------+
| my-web-container | RUNNING | 10.169.24.128 (eth0) |      | CONTAINER | 0         |
+------------------+---------+----------------------+------+-----------+-----------+
```

### Manage containers

```shell
# Stop container
lxc stop my-web-container

# Start container
lxc start my-web-container

# restart container
lxc restart my-web-container

# delete container
lxc delete my-web-container
```

### Exec container

```shell
lxc exec my-web-container -- bash
# exit 
```