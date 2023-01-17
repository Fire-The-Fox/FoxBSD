# /etc/hostname.*

Are files that store configurations for `ifconfig`

## How to create one?

First, run `ifconfig`

The output should have the similar format
```
interface: interface_info
	interface_settings
```

There is one interface that you will have, and that is `lo`, it should be the first one <br>
I also have interfaces such as `re0`, `iwx0` <br>
As root, you can configure specific interface using `ifconfig <interface> ...`, but what if you want to automate it? <br>
That's where `/etc/hostname.*` comes in place <br>

to configure `re0` interface, i need to create `/etc/hostname.re0` <br>
And because that is interface of my ethernet port, all i need to put there is
```
inet autoconf
```

For `iwx0` the filename is `/etc/hostname.iwx0`, etc

## Connecting to wifi - simple way

For me, `iwx0` is my wifi card interface, i'll create `/etc/hostname.iwx0` and write 
```
nwid SSID wpakey PASSWORD
inet autoconf
```
into the file. Replace `SSID` with name of wifi you want to connect to and `PASSWORD` with password of that wifi

## Advanced 
coming soon ...
