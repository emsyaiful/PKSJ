###PENDAHULUAN

Cuckoo Sandbox adalah malware analysis system yang digunakan untuk menganalisis file yang mencurigakan. Cuckoo akan memberikan hasil yang detail apa yang terjadi saat file dijalankan di dalam lingkungan yang terisolasi.

Install Required Package

```$ sudo apt-get install git mongodb libffi-dev build-essential python-django python python-dev python-pip python-pil python-sqlalchemy python-bson python-dpkt python-jinja2 python-magic python-pymongo python-gridfs python-libvirt python-bottle python-pefile python-chardet tcpdump -y ```

Configuring Tcpdump

```$ sudo setcap cap_net_raw,cap_net_admin=eip /usr/sbin/tcpdump```

Installing Yara

````$ sudo apt-get install autoconf libtool libjansson-dev libmagic-dev libssl-dev -y```
```$ wget https://github.com/plusvic/yara/archive/v3.4.0.tar.gz -O yara-3.4.0.tar.gz```
```$ tar -zxf yara-3.4.0.tar.gz```
```$ cd yara-3.4.0```
```$ ./bootstrap.sh```
```$ ./configure --with-crypto --enable-cuckoo --enable-magic```
```$ make```
```$ sudo make install```

To build and install the yara-python extension:

```$ cd yara-python```
```$ python setup.py build```
```$ sudo python setup.py install```

Installing Pydeep

```$ wget http://sourceforge.net/projects/ssdeep/files/ssdeep-2.13/ssdeep-2.13.tar.gz/download -O ssdeep-2.13.tar.gz```
```$ tar -zxf ssdeep-2.13.tar.gz```
```$ cd ssdeep-2.13```
```$ ./configure```
```$ make```
```$ sudo make install```

Installing Volatility

```$ pip install openpyxl```
```$ pip install ujson```
```$ pip install pycrypto```
```$ pip install distorm3```
```$ pip install pytz ```

```$ git clone https://github.com/volatilityfoundation/volatility.git```
```$ cd volatility```
```$ python setup.py build```
```$ python setup.py install```

Installing Cuckoo

```$ git clone git://github.com/cuckoosandbox/cuckoo.git```
```$ useradd cuckoo```
```$ sudo chown -R cuckoo:cuckoo /home/$USER/cuckoo```

Configuring Cuckoo

cuckoo.conf

machinery = virtualbox

[resultserver]
ip = 192.168.56.1 #IP Address host
port = 2042 #default setting

auxiliary.conf

[sniffer]
# Enable or disable the use of an external sniffer (tcpdump) [yes/no].
enabled = yes

# Specify the path to your local installation of tcpdump. Make sure this
# path is correct.
# You can check this using the command: whereis tcpdump
tcpdump = /usr/sbin/tcpdump

# Specify the network interface name on which tcpdump should monitor the
# traffic. Make sure the interface is active.
# The ifconfig command will show you the interface name.
interface = vboxnet0

virtualbox.conf

machines = windowsxp

[windowsxp]
label = windowsxp
platform = windows
ip = 192.168.56.10 # IP Adress guest
snapshot = snapshot1 # nama snapshot

reporting.conf

[mongodb]
enabled = yes

Saatnya Run Cuckoo Sandbox

````$ cd /home/cuckoo/cuckoo```
```$ python cuckoo.py```
