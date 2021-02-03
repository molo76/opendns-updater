# OpenDNS-Updater

OpenDNS's "Dynamic IP" updater is a little opaque, and seems pretty broken on MacOS Big Sur. 

Try using this python script instead, which you can customize for your own needs. This runs in Python3, original repo https://github.com/richgong/opendns-updater has a python2 version. 

## Install

Install required python modules:

`pip3 install -r requirements.txt`

## Configuration

Create a config file called `config.ini` in the same directory:

	[Main]
	label: YourNetworkLabel
	username: your@email.com
	password: your-opendns-password-here

## Run

Run this to update your IP address:

`python3 update.py`

## Not working?

I found that OpenDNS requires that your password contain at least 1 special character. My password contained a couple of these, and it actually caused "HTTP Basic Auth" to break for me. So I changed my password to only contain alphanumeric characters with an underscore as my special character.
