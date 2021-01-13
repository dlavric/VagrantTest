# Pre-Requirements

1.Install the latest version of [Vagrant](https://www.vagrantup.com/docs/installation)
2.Install [VirtualBox](https://www.virtualbox.org/)


# Build the VMs
Check the Vagrantfile from this repository


# Start the VMs

```$ vagrant up```

# Access the VMs

- Web1
```
$ vagrant ssh web1
$ logout
```

- Web 2
```
$ vagrant ssh web2
$ logout
```
# Connect to the Web VMs

- Get the IPs
```$ ipconfig -a```
```
vagrant@vagrant:~$ ifconfig -a
eth0: flags=4163<UP,BROADCAST,RUNNING,MULTICAST>  mtu 1500
        inet 10.0.2.15  netmask 255.255.255.0  broadcast 10.0.2.255
        inet6 fe80::a00:27ff:febb:1475  prefixlen 64  scopeid 0x20<link>
        ether 08:00:27:bb:14:75  txqueuelen 1000  (Ethernet)
        RX packets 642  bytes 82720 (82.7 KB)
        RX errors 0  dropped 0  overruns 0  frame 0
        TX packets 479  bytes 81402 (81.4 KB)
        TX errors 0  dropped 0 overruns 0  carrier 0  collisions 0

lo: flags=73<UP,LOOPBACK,RUNNING>  mtu 65536
        inet 127.0.0.1  netmask 255.0.0.0
        inet6 ::1  prefixlen 128  scopeid 0x10<host>
        loop  txqueuelen 1000  (Local Loopback)
        RX packets 12  bytes 1152 (1.1 KB)
        RX errors 0  dropped 0  overruns 0  frame 0
        TX packets 12  bytes 1152 (1.1 KB)
        TX errors 0  dropped 0 overruns 0  carrier 0  collisions 0
```


- See the Web VM by using the inet IP from the previous command "ipconfig -a"
```
$ curl http://10.0.2.15
```
```
<!DOCTYPE html>
<html>
<head>
<title>Welcome to nginx!</title>
<style>
    body {
        width: 35em;
        margin: 0 auto;
        font-family: Tahoma, Verdana, Arial, sans-serif;
    }
</style>
</head>
<body>
<h1>Welcome to nginx!</h1>
<p>If you see this page, the nginx web server is successfully installed and
working. Further configuration is required.</p>

<p>For online documentation and support please refer to
<a href="http://nginx.org/">nginx.org</a>.<br/>
Commercial support is available at
<a href="http://nginx.com/">nginx.com</a>.</p>

<p><em>Thank you for using nginx.</em></p>
</body>
</html>
```

- Connect to the Web

