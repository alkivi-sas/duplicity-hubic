duplicity backend for hubic
========

Duplicity backend base on the swift one, to use hubic

**This library is unofficial and consequently not maintained by OVH.**

Dependencies
-------
pip python-requests


Installation
-------
Just put hubicbackend.py in the directory of backend (/usr/share/pyshared/duplicity/backends/ or /usr/lib/python2.7/dist-packages/duplicity/backends/)


Use
-------

First generate refresh token using [Hubic Help Page](https://api.hubic.com/sandbox/)


```bash
export HUBIC_CLIENT_ID='api_hubic_djkazdazjkdnjazdnjkazdnkazdnazk'
export HUBIC_CLIENT_SECRET='some_secret'
export HUBIC_REFRESH_TOKEN='your_generated_token'
duplicity --no-encryption /root hubic://default
```

If you already have an access token
```bash
export HUBIC_ACCESS_TOKEN='your_access_token'
duplicity --no-encryption /root hubic://default
```

TODO   
-------
* make a web page to use personnal application and not the sandbox one ...
* make the backend an heritance of swiftbackend

Credits   
-------
Matthieu Huin <mhu@enovance.com> for the original client



License
-------

duplicity-hubic is freely distributable under the terms of the GPLv3 license.
