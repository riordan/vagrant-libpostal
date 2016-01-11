Vagrant Libpostal
==============
[Vagrant](https://www.vagrantup.com) image for working with [libpostal](https://github.com/openvenues/libpostal), all-in-one, i18n friendly address standardization and parsing library.

Provides install for C base, Python bindings (also used for training the model), and [nodejs bindings](https://github.com/openvenues/node-postal).

## Installation
### Pre-requirements:
* Install [VirtualBox](https://www.virtualbox.org/wiki/Downloads)
* Install [Vagrant](http://www.vagrantup.com/downloads)
* Add `ubuntu/trusty64` vm image for your machine
> `vagrant box add ubuntu/trusty64`

## Node bindings

Odds are, you're looking to use the node bindings with a project of yours. In that case, ssh into the machine (`vagrant ssh`), go to your project directory (if you have a working copy in this folder on your filesystem, it'll be in `/vagrant` in the VM) and install it there.

**Node bindings are installed with:**

`npm install openvenues/node-postal`

## iPython notebook
Starting an iPython Notebook is a great way to explore libpostal's capabilities. This Vagrant instance is configured to support using an iPython notebook from your host computer run from inside the Vagrant VM.

**To start an iPython Notebook**
```
cd /vagrant      #or wherever you want your notebook files to be saved
ipython notebook --ip=0.0.0.0
```
Note: It'll try to launch the web browser w3m inside your terminal. It's harmless, but to quit it, type `q` then `y`es.

To stop iPython notebook, press: `ctrl+c` and `y`es

You should be able to get to iPython's web interface on your host machine's browser at: [http://127.0.0.1:8888](http://127.0.0.1:8888).

__NOTE:__ Vagrant will FIGHT YOU if you're already running something on port 8888 (i.e. another iPython notebook) and won't start. You'll have to stop it or change the forwarded port.
