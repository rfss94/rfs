#**Installation**
MITMf relies on a **LOT** of external libraries therefore it is highly recommended you use [virtualenvs](http://docs.python-guide.org/en/latest/dev/virtualenvs/) to install the framework, this avoids permission issues and conflicts with your system site packages (especially on Kali Linux).

Before starting the installation process:

- On Arch Linux:

```
pacman -S python2-setuptools libnetfilter_queue libpcap libjpeg-turbo capstone
```

- On Debian and derivatives (e.g Ubuntu, Kali Linux etc...)

```
apt-get install python-dev python-setuptools libpcap0.8-dev libnetfilter-queue-dev libssl-dev libjpeg-dev libxml2-dev libxslt1-dev libcapstone3 libcapstone-dev libffi-dev file
``` 

#**Installing MITMf**
**Note: if you're rocking Arch Linux: you're awesome! Just remember to use pip2 instead of pip outside of the virtualenv**

- Install virtualenvwrapper: 
```
pip install virtualenvwrapper
```

- Edit your ```.bashrc``` or ```.zshrc``` file to source the virtualenvwrapper.sh script:

```
source /usr/bin/virtualenvwrapper.sh
```
**The location of this script may vary depending on your Linux distro**

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
pip install -r requirements.txt
```

- You're ready to rock! 
```
python mitmf.py --help
```

 