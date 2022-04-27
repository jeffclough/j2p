# j2p
This is a a really simple tool I use to extract and convert constant
definitions from a Java package to Python code.

This project makes heavy use of Chris Thunes's super-helpful
[javalang](https://github.com/c2nes/javalang) python module. And since it
depends on a 3rd-party module, I've set it up to run in a Python virtual
environment. But don't worry. I also provide a simple shell script that makes
running it that way as easy as running any other script on your path.

## Installation

1. Clone this repo into your own filespace. I'm using ~/venvs/j2p for this.
```shell
mkdir ~/venvs
git clone git@github.com:jeffclough/j2p.git ~/venvs/j2p
```

2. Initialize the virtual environment is your local repo.
```shell
cd ~/venvs/j2p
python3 -m venv .
source bin/activate
pip install -r requirements.txt
deactivate
```

3. Add a symlink to ~/venvs/jp2/runner from someplace on your PATH.
```shell
cd ~/my/bin
ln -s ~/venvs/j2p/runner j2p
```

### Testing Installation

You should now be able to run j2p from anyplace without having to activate it
first. 

```
% j2p -h
usage: j2p [-h] [--debugger] FILE

Read the java package source from the file named on the command line. Write
the equivalent Python constant definitions to standard output. This is a
fairly primitive Java interpreter, and there's not much thought given to error
messages. Be sure to give it a valid, complete Java package source file.

positional arguments:
  FILE        Name of the file containing the Java package in question.

optional arguments:
  -h, --help  show this help message and exit
  --debugger  Engages the Python debugger. See "Debugger Commands" section of
              https://docs.python.org/3/library/pdb.html for documentation.
```

I don't recommend using j2p's --debugger option. It's really just for me to
use while figuring out the particulars of using javalang.

## Running j2p

I'll elaborate at some point. For now, see the usage statement above.
