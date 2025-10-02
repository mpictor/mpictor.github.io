+++
date = 2020-05-06T23:48:48-05:00
draft = false
title = 'Firstest or worstest'
summary = 'Magic SysRq and the blog name'
tags = ["first", "naming","sysrq","linux"]
+++

So I decided to try out hugo. Gonna weblog like it's 1999. No, no, not quite... gonna gopher like it's port 70? That'll work.

###### As long as nobody actually tries port 70.

----

...so what's all this REISUB stuff anyhow? (with apologies to Bob Pease)

SysRq is a key found on most PC keyboards. It was introduced by IBM, back when they were the dominant force in personal computers. About the only use for it is if you run Linux (or perhaps an experimental OS). In Linux, if "Magic SysRq" is enabled, you can input key sequences useful in disaster recovery.

The sequences generally aren't useful except in a situation (disaster) where the system is no longer responsive. The sequences involve holding down `Alt`, then tapping `SysRq` followed by one or more other keys. If I recall correctly, some keyboards do not actually send `SysRq` unless you hold down additional keys (such as `Shift`) while tapping `SysRq`.

The two magic sequences I've used the most are `R E I S U B` and `R E I S U O`, differing only in the last letter.
* r: switch keyboard from raw (X11) mode
* e: SIGTERM all processes except init
* i: SIGKILL all processes except init
* s: sync all mounted filesystems
* u: remount everything read-only
* b: *immediate* reboot
* o: *immediate* power off

As you can see, most of these would be catastrophic to a running system. `s` won't break anything, and many apps would mostly continue to function after `u` - but those are the only benign ones. 

`b` and `o` really are immediate: if used on their own, they are equivalent to yanking the power cord and are likely to result in lost data and/or filesystem errors.

So why did I choose REISUB as the name of this blog? Because naming things is hard. People have already claimed `EAGAIN`, `xor EAX EAX EAX`, and many others I'd consider.

Don't read too much into the name: this blog isn't likely to be of much use in disastrous situations.
