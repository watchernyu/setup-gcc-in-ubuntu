This is tested in a ubuntu docker container. 

If "add-apt-repository" is missing, then first `apt install software-properties-common`

`gcc --version` will check the current version of your gcc.

Go to `/usr/bin` (on mac might be `/usr/local/bin`), `ls gcc*` to find all gcc versions. For example, if we need gcc-10 and g++-10:

```
sudo add-apt-repository ppa:ubuntu-toolchain-r/test
sudo apt-get update
sudo apt install gcc-10
sudo apt install g++-10
```

Now should be able to see these in `/usr/bin`.

Use a symbolic link to point the default gcc to the gcc we want to use. In the `/usr/bin` folder,

```
rm gcc
rm g++
ln -s gcc-10 gcc
ln -s g++-10 g++
```


