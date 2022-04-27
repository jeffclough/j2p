# j2p
This is a a really simple tool I use to extract and convert constant
definitions from Java code to Python code.

## Installation
Once you've cloned this repo to your own filespace (e.g. ~/venvs/j2p),
initialize the virtual environment there as follows:

Get the j2p script, and set it up in a Python virtual environment.

```shell
cd ~/venvs/j2p
python3 -m venv .
source bin/activate
pip install -r requirements.txt
deactivate
```

Add a symlink to ~/venvs/jp2/runner from someplace on your PATH.

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

## Running j2p

I'll elaborate at some point. For now, see the usage statement above.
