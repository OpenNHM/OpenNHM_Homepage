---
title: "This month in AvaFrame - July 2022 edition"
date: 2022-08-05T00:00:00+01:00
draft: false
---

Welcome to the July 2022 update.

This month, despite being one of the *slow* summer month, we speed up our computation. 
Some variable are only computed if they are actually requested, so for most simulations this leads to faster compute times. 

In preparation for a bigger overhaul of the AvaFrameConnector (QGis) we started adding helper functions that are used by the connector. 
These functions contain stuff like layer renaming and similar stuff that makes handling the result a bit easier. 
This will end up in the next version expected to be out in the next few months. 

For the developers we added a new way of overriding default configurations, in case your module needs a certain, fixed setup of another module. 
If you search for *modName_override* you will find examples of the usage. Again, this is for people working with the script version (not QGis).

That's it for this month,

Felix
