---
layout: post
title: You don't need MAC address cloning
---

> Comcast, technically, only “knows” the MAC address of the *modem*. Putting this address into their database is what they call “provisioning”. Permission-to-talk is granted to your modem by the CMTS (head end) based upon this entry. Your modem, in turn, is configured to talk to one MAC address – any MAC address – the first that tries to talk via its ethernet port.
>
>The problem is that once the modem sees a MAC address, it firmly remembers it. Takes about a 30 second power-cycle to make it forget. Makes it annoying when switching between two devices - a Mac and an Airport, in this case.
>
> (Quoted from http://forums.xfinity.com/t5/Macintosh/Airport-Extreme-and-Comcast/td-p/27505)

I have been using a traditional LinkSys 11g wireless router
with the MAC address cloning to avoid this problem.
But Apple's AirPort Extreme, which I bought lately,
doesn't have this feature and I was in trouble again.

I googled around for a while and eventually found  
this article, and the problem is now gone.
