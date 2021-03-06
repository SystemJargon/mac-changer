## MAC Changer 

Reference to the tool used in GNU / Unix to manipulate MAC addresses.


GNU MAC Changer is an utility that makes the maniputation of MAC
addresses of network interfaces easier.

I also made this in light of seeing square [here](https://github.com/EmreTech/square) and [here](https://github.com/NoahCardoza/square), this maybe a way easier method. 

Not that I use Disney Circle, but I am currently writing a paper on DNS with security as a highlight of sorts.

----

## How to use it

Show MAC address
```
macchanger -s
```

Set Random MAC address
 
```
ifconfig wlan0 down
macchanger -r wlan0 
ifconfig wlan0 up
```

Set random vendor MAC of the same kind
```
ifconfig wlan0 down
macchanger -ab wlan0 
ifconfig wlan0 up
```
Reset to original, permanent hardware MAC

```
ifconfig wlan0 down
macchanger -p wlan0 
ifconfig wlan0 up
```




* If using ethernet replace wlan0 with eth0 or eno1 or whatever interface name is used. "ifconfig" is your friend.

* Note, some people believe you may or may not have to bring down and up the interface after each change or, restart the network service in Debian. RedHat, CentOS may differ.


----

## Help context
```
$ macchanger --help
GNU MAC Changer
Usage: macchanger [options] device

  -h,  --help                   Print this help
  -V,  --version                Print version and exit
  -s,  --show                   Print the MAC address and exit
  -e,  --ending                 Don't change the vendor bytes
  -a,  --another                Set random vendor MAC of the same kind
  -A                            Set random vendor MAC of any kind
  -p,  --permanent              Reset to original, permanent hardware MAC
  -r,  --random                 Set fully random MAC
  -l,  --list[=keyword]         Print known vendors
  -b,  --bia                    Pretend to be a burned-in-address
  -m,  --mac=XX:XX:XX:XX:XX:XX
       --mac XX:XX:XX:XX:XX:XX  Set the MAC XX:XX:XX:XX:XX:XX

Report bugs to https://github.com/alobbs/macchanger/issues
```
----

## Further Links

[GNU macchanger Author](https://github.com/alobbs/macchanger) - LEGEND!

[Debian packages](https://packages.debian.org/bullseye/macchanger)

[Debian_amd64](http://ftp.nz.debian.org/debian/pool/main/m/macchanger/macchanger_1.7.0-5.4_amd64.deb) or

[Debian_i386](http://ftp.nz.debian.org/debian/pool/main/m/macchanger/macchanger_1.7.0-5.4_i386.deb)

----

## Alternative download and install method / how-to

```

wget -O ~/downloads/macchanger_1.7.deb http://ftp.nz.debian.org/debian/pool/main/m/macchanger/macchanger_1.7.0-5.4_amd64.deb

sudo dpkg -i ~/downloads/macchanger_1.7.deb
```

