# Install `Advanced Copy` patch to add Progrees Bar to `cp` and `mv` command in linux

## Dowload latest `GNU coreutils`

>`wget http://ftp.gnu.org/gnu/coreutils/coreutils-8.32.tar.xz`

### Extract the download archive

>`tar xvJF coreutils-8.32.tar.xz`

### Goto that directory

>`cd coreutils-8.32/`

### Download the Advanced Copy patch

>`wget https://raw.githubusercontent.com/jarun/advcpmv/master/advcpmv-0.8-8.32.patch`

### Apply the patch

> `patch -p1 -i advcpmv-0.8-8.32.patch`
> `./configure`
> `make`

### Now two new patched binaries namely `cp` and `mv` will be created in the `coreutils-8.32/src` folder. Just copy them to your $PATH like below

> `sudo cp src/cp /usr/local/bin/cp`
> `sudo cp src/mv /usr/local/bin/mv`

### Whenever you want a progress bar while copying or moving files and directories, just add`-g` flag like below

> `cp -g source destination`

### Or use `--progress-bar` flag

> `cp -progress-bar source destination`
