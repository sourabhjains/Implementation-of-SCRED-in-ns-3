# Implementation of Self Configuring RED (SCRED) algorithm in ns-3
## Course Code: CS822
## Assignment: # GP3

### Overview

Self Configuring RED (SCRED) [1] is a variant of Random Early Detection (RED) [2], it makes RED parameters adaptive to handle wide variety of traffic. This repository provides an implementation of SCRED in ns-3.25 [3].

### Simulating SCRED 

To simulate SCRED algorithm, the attribute FengAdaptive must be set to true, as shown below:

`Config::SetDefault ("ns3::RedQueueDisc::FengAdaptive", BooleanValue (true));`

### SCRED example

An example program for SCRED has been provided in

`src/traffic-control/examples/red-vs-scred.cc`

and should be executed as

`./waf --run "red-vs-scred --queueDiscType=FengAdaptive"`


### References:

[1] Feng, W. C., Kandlur, D. D., Saha, D., & Shin, K. G. (1999, March). A self-configuring RED gateway. In INFOCOM'99. Eighteenth Annual Joint Conference of the IEEE Computer and Communications Societies. Proceedings. IEEE (Vol. 3, pp. 1320-1328). IEEE.

[2] Floyd, S., & Jacobson, V. (1993). Random early detection gateways for congestion avoidance. IEEE/ACM Transactions on networking, 1(4), 397-413.


[3] https://www.nsnam.org/ns-3-25/
