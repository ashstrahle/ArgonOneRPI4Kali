#!/bin/bash
echo "-------------------------"
echo "Argon One Uninstall Tool"
echo "-------------------------"
echo -n "Press Y to continue:"
read -n 1 confirm
echo
if [ "$confirm" = "y" ]
then
	confirm="Y"
fi

if [ "$confirm" != "Y" ]
then
	echo "Cancelled"
	exit
fi
if [ -d "/home/pi/Desktop" ]; then
	sudo rm "/home/pi/Desktop/argonone-config.desktop"
	sudo rm "/home/pi/Desktop/argonone-uninstall.desktop"
fi
if [ -f /usr/bin/argononed.py ]; then
	sudo systemctl stop argononed.service
	sudo systemctl disable argononed.service
	sudo /usr/bin/python3 /lib/systemd/system-shutdown/argononed-poweroff.py uninstall
	sudo rm /usr/bin/argononed.py
	sudo rm /lib/systemd/system-shutdown/argononed-poweroff.py
	sudo rm /usr/bin/argonone-uninstall
	echo "Removed Argon One Services."
	echo "Cleanup will complete after restarting the device."
fi
