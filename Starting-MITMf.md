#**Starting MITMf**
At it's core, MITMf is just a supped of version of [SSLstrip](https://github.com/moxie0/sslstrip) with some tricks up it's sleeve.

When you start MITMf with the command: 
```
python mitmf.py -i interface
```

A few things happen:
- The SSLstrip proxy starts and load any plugins we called from the command line

The SSLStrip proxy will intercept any HTTP traffic and modify it to our bidding
 
- An HTTP, DNS and SMB server are started

These servers are primarily used in conjunction with the frameworks plugins
 
- [NetCreds](https://github.com/DanMcInerney/net-creds) is started

An awesome tool by an awesome guy! [NetCreds](https://github.com/DanMcInerney/net-creds) job is to sniff (at Layer 3) any and all clear-text credentials going over the wire

- MITMf-API webserver is started

The MITMF-API webserver exposes an API which can be used to enable and disable plugins on the fly

