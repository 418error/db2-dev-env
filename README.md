# db2-dev-env
This started off as a work related thing. Showing how simple it could be talking back to our legacy DB2 instance running on a mainframe using a lite weight framework like [Java spark][Java Spark].

As I was proving this off our network I spun up this environment with DB2 Express-C, a free to develop, free to deploy and free to distribute version of DB2.

## Prerequisites
I'm on a Mac using Homebrew goodness...

virtualbox
```
• brew cask install virtualbox
```
• vagrant
```
brew cask install vagrant
```
• vagrant trigger plugin
```
vagrant plugin install vagrant-triggers
```

## Get the Env running...

Download DB2 Express-C from IBM at the time of writing the version was 10.5 (v10.5_linuxx64_expc.tar.gz) and place it here with the vagrant file.

```
vagrant up
```
ignore the following error message...

```
==> default: Requirement not matched for DB2 database "Server" . Version: "10.5.0.5".
==> default:
==> default: Summary of prerequisites that are not met on the current system:
==> default:
==> default:    DBT3514W  The db2prereqcheck utility failed to find the following 32-bit library file: "/lib/libpam.so*".
==> default:
==> default:
==> default: DBT3514W  The db2prereqcheck utility failed to find the following 32-bit library file: "libstdc++.so.6".
```

You now have a running instance of DB2 with the out of the box sample database.

For an example API designed for this dev env go to [db2-spark-example page][db2-spark-example page]

[IBM DB2 Lite download page]:http://www-01.ibm.com/software/data/db2/express-c/download.html
[db2-spark-example page]:https://github.com/lendmeapound/db2-spark-example
