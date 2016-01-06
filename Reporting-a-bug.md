#**Bug Reporting**

Bug reporting is an essential part of any project since it let's people know whats broken!

Before reading on, here's a list of cases where you **shouldn't** be reporting the bug:
- If you haven't installed MITMf using the method described in the [installation intructions](https://github.com/byt3bl33d3r/MITMf/wiki/Installation). (your fault!)
- If you're using an old version of the framework (by old I mean anything else that **isn't** the current version on Github)
- If you found a bug in a packaged version of MITMf (e.g. Kali Repos), please file a bug report with the distros maintainer
- If you're issue isn't a bug but a general question about the framework, please only open a ticket for bugs **not** questions. If you have any questions please email me at byt3bl33d3r@gmail.com

Lately, there has been a sharp increase in the volume of bug reports, so in order for me to make any sense out of them and to quickly identify, reproduce and push a fix I do pretend a minimal amount of cooperation from the reporter!

#**Writing the report**
**Before submitting a bug familiarize yourself with [Github markdown](https://help.github.com/articles/github-flavored-markdown/) and use it in your report!**

After that, open an issue ticket and please describe the bug in **detail!** MITMf has a lot of moving parts so the more detail the better!

Every report should include:
- The full command string you used
- The full output of: ```pip freeze```
- The full output of MITMf in debug mode (append ```--log debug``` to the command you used)
- The OS you're using (distribution and architecture)
- The full error traceback (If any)
- If the bug resides in the way MITMf sends/receives packets, include a link to a pcap containing a full packet capture

**If a report doesn't contain all of the above, it will probably be ignored!**

#**Some good & bad examples**

https://github.com/byt3bl33d3r/MITMf/issues/71

https://github.com/byt3bl33d3r/MITMf/issues/70

https://github.com/byt3bl33d3r/MITMf/issues/64

#Punishment for writing a bad bug report, not making any sense or asking stupid questions

I will probably link you to a random youtube video that I think is hilarious in the context of the issue title or text and add the dafuq?, srsly? tags