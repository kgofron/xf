```
IOC migration
•	Finish cameras – DONE, Naming 9/25 revisited.
•	MC15 (smaract controller for saxs beamstops). Test mc15, Migrate mc16 later. Smarpod (migrate).
•	Prep other iocs, many will need to be tested with beam
o	Trigger – build, not start it.
o	Vacuum. Va-1. 2 ion pumps, trurbo for sample. SAX instrument – 
o	Dlm - tricky

Debug problem with 3 SmarAct axes (mbs-ib, BPM diodes) in FOE. Xf11ida-ioc1/mc5 (Inboad,X/Y; 0/1/2); Alex will test
	Need to be very careful not to move any axes, as otherwise finding the beam after the shutdown might be very difficult
	Alex might inspect the module 0.
Configure network switch: net-11id1-agg  port #1 for 10.11.2 (to permanently install moxa plc). Ticket (IPs are assigned). 
Running out of ports on switch for XF11id-B -> need another switch for ‘general purpose’ (motion controller, camera,…). Ticket send.
Install/test smarpod (ioc existed, needs to be migrated & tested?) -> this is new hardware, nominally bought what we used to borrow. B-hutch project.
Upgrade firmware on EIger500k to fix bug related to switching between 12 and 4 bit modes. Firmware/ possible EPICS driver issues. This shutdown, or December.

Printer setups
Printer 1 -> migration to new computing rack, new version of Debian (9?). Exists, but need to change. Migrate to new computer.
-	Upgrade OS to Deb 9(?). 
-	Iocs to migrate: couple of cameras (prosiclica/blackfly), smaract MCS2, UV light. Limits detection
-	Develop simple ioc for dispenser. Pressure pump.

Printer 2 (new setup). Build from scratch. Hardware exists.
-	Upgrade OS (Deb 9?)
-	Install (custom) DT
-	SmarAct MCS2
-	Cabling for PI stages + inhouse motion stage (Scott design)
-	Iocs for moxa, UV, hyrel,….
-	Bunch of cameras (BFLY and Grasshopper) 
```

```
ioLogick units
```
