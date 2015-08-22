#**Installation**
MITMf relies on a LOT of external libraries therefore it is highly recommended you use [virtualenvs](http://docs.python-guide.org/en/latest/dev/virtualenvs/) to install them in, this avoids permission issues and conflicts with your system site packages (especially on Kali Linux).

- Install virtualenvwrapper: 

```
pip install virtualenvwrapper
```

- Edit your ```.bashrc``` or ```.zshrc``` file to source the virtualenvwrapper.sh script:

```
source /usr/bin/virtualenvwrapper.sh
```

- Restart your terminal or run: 

```
source /usr/bin/virtualenvwrapper.sh
```

- Create your virtualenv: 

```
mkvirtualenv MITMf -p /usr/bin/python2.7
```

- Clone the MITMf repository: 

```
git clone https://github.com/byt3bl33d3r/MITMf
```

- cd into the directory, initialize and clone the repos submodules: 

```
cd MITMf && git submodule init && git submodule update --recursive
```

-  Install the dependencies: 

```
pip install install -r requirements.txt
```

- You're ready to rock! 
```
python mitmf.py --help
```

 