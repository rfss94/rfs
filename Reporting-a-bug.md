#**Bug Reporting**

Bug reporting is an essential part of any project since it let's people know whats broken!

Before reading on, here's a list of cases where you **shouldn't** be reporting the bug:
- If you haven't installed MITMf using method described in the [installation](https://github.com/byt3bl33d3r/MITMf/wiki/Installation) intructions. (your fault!)
- If you're using and old version of the framework (and by old I mean anything else that **isn't** the current version on Github)

Lately, there has been a sharp **increase** in the volume of bug reports so in order for me to make any sense out of them and to quickly identify, reproduce and push a fix I do pretend a minimal amount of cooperation from the reporter!

#**Writing the report**
**Before submitting a bug familiarize yourself with [Github markdown](https://help.github.com/articles/github-flavored-markdown/) and use it in your report!**

After that, open an issue ticket and please describe the bug in **detail!** MITMf has a lot of moving parts so the more detail the better!

Include in the report:
- The full command string you used
- The full output of MITMf in debug mode (append ```--log debug``` to the command you used)
- The OS you're using (distribution and architecture)
- The full error traceback (If any)
- If the bug resides in the way MITMf sends/receives packets, include a link to a pcap containing a full packet capture