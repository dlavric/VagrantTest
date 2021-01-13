# VagrantTest

This is my first Vagrant VM

- Start the VM

```$ vagrant up```

- Access the VMs: 

- Web1
```$ vagrant ssh web1

$ ipconfig -a

// Check the inet for the hostname, from the previous command _ipconfig -a_
$ curl http://hostname

$ logout
```

- Web2
```$ vagrant ssh web2

$ ipconfig -a

// Check the inet for the hostname
$ curl http://hostname

$ logout
```
