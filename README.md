# OpenSesame

OpenSesame is a tool to create experiments for psychology, neuroscience, and experimental economics.

Copyright, 2010-2017, Sebastiaan Mathôt and contributors.

http://osdoc.cogsci.nl/

## Building & Running on Python 3

Create a fresh Python virtual environment and install prerequisites:

```
python3 -m venv .
source bin/activate
pip3 install PyQt5 qtpy QScintilla PyQtWebEngine markdown ipykernel==4.6.1 qtconsole
sudo apt install libyaml-cpp-dev
```

Now clone the source code, build and run:

```
git clone https://github.com/dmikushin/OpenSesame
cd OpenSesame
python3 setup.py install
./opensesame
```

## Troubleshooting

I was kept getting this on startup:

```
QObject::setParent: Cannot set parent, new parent is in a different thread
Trace/breakpoint trap (core dumped)
```

This comes from class `IPythonImporter(QtCore.QThread)` used to initialize IPython in a separate thread. Did not work until `ipykernel==4.6.1` (which [https://osdoc.cogsci.nl/3.2/dev/fromsource/#icon-theme](OpenSesame docs) mention as "optional") and `qtconsole` have beed installed as shown above.

