###PENDAHULUAN###

####Cowrie SSH Honeypot###

"Cowrie is a medium interaction SSH and Telnet honeypot designed to log brute force attacks and the shell interaction performed by the attacker."

Cowrie dikembangkan oleh Michel Oosterhof.

####Fitur-fitur Cowrie

1. Fake filesystem with the ability to add/remove files. A full fake filesystem resembling a Debian 5.0 installation is included
1. Possibility of adding fake file contents so the attacker can cat files such as /etc/passwd. Only minimal file contents are included
1. Session logs stored in an UML Compatible format for easy replay with original timings
1. Cowrie saves files downloaded with wget/curl or uploaded with SFTP and scp for later inspection


Additional functionality over standard kippo:

1. SFTP and SCP support for file upload
1. Support for SSH exec commands
1. Logging of direct-tcp connection attempts (ssh proxying)
1. Forward SMTP connections to SMTP Honeypot (e.g. mailoney)
1. Logging in JSON format for easy processing in log management solutions
1. Many, many additional commands
1. Requirements

####Software requirements:####

1. Python 2.7+, (Python 3 not yet supported due to Twisted dependencies)
1. Zope Interface 3.6.0+
1. Twisted 12.0+
1. python-crypto
1. python-cryptography
1. python-pyasn1
1. python-gmpy2 (recommended)
1. python-mysqldb (for MySQL output)
1. python-OpenSSL