# .dotfiles
A collection of various configuration files

## Installing
\[ **WARNING** \] This command will overwrite any file that already exists in this
repository, like your .bashrc, make sure to backup your files before running
this command.\
Run this command in your home directory to install everything automatically.
```
git clone --no-hardlinks --no-checkout https://github.com/dretez/.dotfiles.git tmp &&
mv tmp/.git/ . &&
rm -rf tmp/ &&
git restore --staged . &&
git restore . &&
git submodule update --init --recursive
```

## Maintaining
This command will pull both new commits from this repository, as well as from
all submodules. Should any submodules have new commits, remember to commit the
updated submodules to this repository.
```
git fetch &&
git pull &&
git submodule update --remote --merge
```
