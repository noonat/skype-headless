skype-headless
--------------

Vagrantfile to run Skype on an Ubuntu VM, along with the requirements
for the Python Skype4Py (so that you can script your headless Skype).
Services are managed by Upstart.

To use:

- Edit provision/run-skype.sh and change the username and password.
- Edit provision/x11vnc.conf and change the password.
- Run vagrant up.
- VNC to 192.168.33.10:5900.

[Skype4Py] is installed to a virtualenv in /home/vagrant/env.

[Skype4Py]: https://github.com/awahlig/skype4py

