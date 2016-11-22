# Gorjanc Shell
Gregor Gorjanc's (bash) shell functions and scripts

## Description

A set of functions and scripts that make my life easier when working in shell/terminal.

The functions/scripts are:
  * [cwdiff](cwdiff) color word diff (originally from Iain Murray)

## Installation

Functions are stored in files named *func_foo.sh* while scripts are stored in
files named *foo*.

1. Save the files in your ~/bin folder
2. Add ~/bin folder to your PATH variable, i.e., export PATH=~/bin:$PATH
3. In order to be able to use functions, add the following code to your ~/.bashrc
file for each function you want to use:

```shell
if [ -f ~/bin/func_foo.sh ]; then
  source ~/bin/func_foo.sh
fi
```

or for a set of functions:

```shell
FUNCS="func_foo1.sh
       func_foo2.sh"
for FILE in ${FUNCS}; do
  if [ -f "~/bin/${FILE}" ]; then
    source ~/bin/${FILE}
  fi
done
```
