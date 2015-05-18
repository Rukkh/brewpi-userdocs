Installing python requirements
==============================

The Raspbian Wheezy images comes with python 2.7 already installed, but BrewPi uses a few python modules that you have to install yourself:

* `pySerial <http://pyserial.sourceforge.net/pyserial_api.html>`_ For communication with the Arduino.
* `simplejson <http://simplejson.github.com/simplejson/>`_ To encode and decode JSON objects. Easier to use than the default JSON module.
* `ConfigObj <http://www.voidspace.org.uk/python/configobj.html>`_  For configuration files support.
* `psutil <http://pythonhosted.org/psutil/>`_ To view running processes and close/kill them from within python
* `GitPython <http://gitpython.readthedocs.org/en/latest/intro.html>`_ A Python library to work with git repositories. Used by the update script.

All 5 modules can be easily installed with apt-get:

.. code-block:: bash

    sudo apt-get install python-serial python-simplejson python-configobj python-psutil python-git

If you're not using a raspberryPi or other linux distro with apt-get available, you can alternatively use the python installer:

.. code-block:: pycon

	pip install pyserial simplejson configobj psutil gitpython
	
Finally, the python script can reprogram the Arduino, but it needs avrdude to do so. Install arduino-core, which includes avrdude.

.. code-block:: bash

    sudo apt-get install arduino-core

That's it, everything is ready for running the BrewPi script. Let's get it from GitHub in the next step.
