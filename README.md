This repository has a set of tools that will be available from the cross compilation system (see xbuilder for more information).

# Tools
## createpkg
Can be used to easily create a deb file that can be distributed. Note this is not a packaging method approved by any Ubuntu or Debian leaders.

Example:
```
git clone kde:kate
cd kate
mkdir build
cd build
cmake .. -DKDE_INSTALL_USE_QT_SYS_PATHS=ON -DCMAKE_INSTALL_PREFIX=/usr #note we want the actual final destination
make -j4
createpkg kate
```
Disclaimer: Example not tested.

This will create a package that doesn't specify dependencies and with a really high version. Keep that in mind.

## deploypkg
TODOCUMENT

## cloneprocess
Lets you run a process, using the environment variables of another process.

```
cloneprocess <pid> [command args...]
```

## click-get
Downloads a file using ubuntu's oauth information.

```
click-get <url>
```

It will ask for an email and password, which are the login information in login.ubuntu.com.

