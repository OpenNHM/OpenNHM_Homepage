---
title: "This month in AvaFrame - August 2022 edition"
date: 2022-09-05T00:00:00+01:00
draft: false
---

Welcome to the August 2022 update.

This month saw us adding a rotational energy line test which can be used to checks eg. for numerical grid independence,
i.e. the computations lead to the same results irrespective of the grid orientation. This includes helper functions and test data,
see test case avaBowl. 

Again, in preparation for the upcoming release, we changed the logic for the secondary release areas. So far they had to be requested
specifically. Now they are included IF there are shapefiles in the SECREL directory (and not forced to be off). 
This will allow for easy inclusion of secondary releases from the AvaFrameConnector (QGis). 

Aimec got some improvement, both in function and the documentation. We added surface parallel coordinate computation as an option to 
run analysis. 

Another ongoing work is the writing of a  theory paper for com1DFA, expected to be submitted in fall. 

And last but not least the AvaFrame Steering Meeting took place. So far we are on track with this project...

Felix
