py-libzfs
======

**Python bindings for libzfs**

py-libzfs is a fairly straight-forward set of Python bindings for libzfs for ZFS on Linux and FreeBSD.

**Jays' Notes**

* Dependencies in `debian/control` have been updated to refer to packages that actually exist in modern Ubuntu repositories.
* `Makefile.in` has had its `PYTHON` definition changed to a more reasonable value.

Build and install by running:

```bash
./configure --prefix=/usr
make
sudo make install
```

Build `.deb` package by running:

```bash
dpkg-buildpackage -b -rfakeroot -us -uc
```

**INSTALLATION**

`./configure && make install`

***MacOS and O3X***

Before runnig configure script, clone O3X repository:

`git clone https://github.com/openzfsonosx/zfs.git ../zfs`

**FEATURES:**
- Access to pools, datasets, snapshots, properties, pool disks
- Many others!

**QUICK HOWTO:**

`import libzfs`

Get a list of pools:

`pools = list(libzfs.ZFS().pools)`

Get help:

`help(libzfs)`


