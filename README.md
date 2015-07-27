# h2o

This is Dockerfile for trying [h2o](https://github.com/h2o/h2o).

To Build,

```bash
$ docker build -t zchee/h2o .
```

To run,

```bash
$ docker run --rm -p <port>:<port> zchee/h2o examples/h2o/h2o.conf
```

To custom config file run,

```bash
$ docker run --rm -p <port>:<port> zchee/h2o h2o.conf
```

sysctl.conf

```
net.core.somaxconn=32768
net.core.netdev_max_backlog=32768
net.ipv4.tcp_max_syn_backlog=32768
net.ipv4.tcp_tw_recycle=1
net.ipv4.tcp_tw_reuse=1
net.ipv4.tcp_fin_timeout=10
net.core.rmem_max  = 16777216
net.core.wmem_max  = 16777216
net.ipv4.tcp_rmem  = 4096 349520 16777216
net.ipv4.tcp_wmem  = 4096 65536 16777216
net.ipv4.ip_local_port_range= 1024 65535
net.ipv4.tcp_timestamps = 0
```
