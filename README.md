winning
=======

This is an installer that sets up mining software for the Bitcoin network with sane defaults, optionally installing Bitcoin and P2Pool locally.

## Tools

### Required
1. [BFGMiner](http://luke.dashjr.org/programs/bitcoin/files/bfgminer/latest/)
2. [cgminer](http://ck.kolivas.org/apps/cgminer/)

### Optional
1. [Bitcoin](http://sourceforge.net/projects/bitcoin/)
  * [Bootstrap.dat](http://sourceforge.net/projects/bitcoin/files/Bitcoin/blockchain/bootstrap.dat.torrent/download)
2. [P2Pool](http://p2pool.in/)
  * [Python 2.7](http://www.python.org/ftp/python/2.7.6/python-2.7.6.msi) [x64](http://www.python.org/ftp/python/2.7.6/python-2.7.6.amd64.msi)
  * [Twisted](http://twistedmatrix.com/Releases/Twisted/13.2/Twisted-13.2.0.win32-py2.7.msi) [x64](http://twistedmatrix.com/Releases/Twisted/13.2/Twisted-13.2.0.win-amd64-py2.7.msi)
  * [Zope](https://pypi.python.org/packages/2.7/z/zope.interface/zope.interface-3.8.0.win32-py2.7.exe#md5=ddb6ff27c106ca39d9f03402a3bcb2a1) [x64](https://pypi.python.org/packages/2.7/z/zope.interface/zope.interface-3.8.0.win-amd64-py2.7.exe#md5=92d66872d65bfcf74aaf137c956608ff)
  * [pywin32](http://sourceforge.net/projects/pywin32/files/pywin32/Build%20218/pywin32-218.win32-py2.7.exe/download) [x64](http://sourceforge.net/projects/pywin32/files/pywin32/Build%20218/pywin32-218.win-amd64-py2.7.exe/download)
  * [wmi](https://pypi.python.org/packages/any/W/WMI/WMI-1.4.9.win32.exe#md5=31ef47dc10ff13a81a0cb8e6a98a0819)

## Installation

* [WiX](http://wixtoolset.org/)
* [NSIS](http://nsis.sourceforge.net)
* [Inno Setup](http://www.jrsoftware.org/isinfo.php)
* [wpkg](http://windowspackager.org/)

## Pseudo-code

	user-option: bfgminer | cgminer
	 download latest miner
	 install miner

	user-info: bitcoin-address
	 validate address

	create setup file
	 insert pool info
	  [eligius](http://eligius.st)
	  [p2pool](http://p2pool.in/)
	 add bitcoin-address

	user-option: run local p2pool
	 user-option: install bitcoind
	  generate rpc password
	  set conf server=1
	  suggest bootstrap.dat

	user-option: start-on-boot
	 add registry entry

## Enhancements

1. Automatic updates
2. Important notifications
