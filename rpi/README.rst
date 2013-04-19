1. Find the rpi with ``arp -a``. You probably want one with a MAC address
   starting with ``b8:27:eb``
2. ``ssh-copy-id pi@<ip>``
3. ``raspi-config`` (https://github.com/shamiao/raspi-autoconfig?)
4. Add to ansible hosts file under ``[rpi]``
4. ansible-playbook --sudo rpi/main.yml
