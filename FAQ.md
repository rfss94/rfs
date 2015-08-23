#**Frequently asked questions**
- **Is Windows supported?**
- Nope, it will never be supported

- **Is OSX supported?**
- Nope, Initially OSX support was on the table, unfortunately as of 0.9.8 MITMf needs a very Linux specific library for active packet filtering support

- **I can't install package X because of an error!**
- Try installing the package via ```pip``` or your distro's package manager. This is a problem with your system setup and not MITMf.

- **```MITMf``` sometimes does not work properly, it seems the problem is about ARP Spoofer. What should i do?**
- This is nothing to do with ```MITMf```, this is caused by ```scapy``` bug. Please consider following patch for ```scapy-2.2.0```. Also you can adapt it to other versions.

```
--- sendrecv.py.ori	2015-07-07 08:45:30.919945734 +0000
+++ sendrecv.py	2015-07-07 08:46:43.619947099 +0000
@@ -17,6 +17,7 @@
 import plist
 from error import log_runtime,log_interactive
 from base_classes import SetGen
+import errno
 
 #################
 ## Debug class ##
@@ -126,7 +127,11 @@
                                 if len(inp) == 0 or pks in inp:
                                     r = pks.nonblock_recv()
                             else:
-                                inp, out, err = select(inmask,[],[], remaintime)
+                                inp = []
+                                try:
+                                    inp, out, err = select(inmask,[],[], remaintime)
+                                except Exception,e:
+                                    if e[0] != errno.EINTR: raise
                                 if len(inp) == 0:
                                     break
                                 if pks in inp
```