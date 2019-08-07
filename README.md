# OpenSesame

OpenSesame is a tool to create experiments for psychology, neuroscience, and experimental economics.

Copyright, 2010-2017, Sebastiaan Mathôt and contributors.

http://osdoc.cogsci.nl/

## Building & Running on Python 3

Create a fresh Python virtual environment and install prerequisites:

```
python3 -m venv .
source bin/activate
pip3 install PyQt5 qtpy QScintilla PyQtWebEngine
sudo apt install libyaml-cpp-dev
```

Now clone the source code, build and run:

```
git clone https://github.com/dmikushin/OpenSesame
cd OpenSesame
python3 setup.py install
./opensesame
```

