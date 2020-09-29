# IOC migration from xf11idb-ioc1 (Deb 7) to xf11idb-ioc2 (Deb 9)

| 11ID-B | DNS          |  | OS       | HW  |
|--------|--------------|--|----------|-----|
| src    | xf11idb-ioc1 |  | Debian 7 | IBM |
| dest   | xf11idb-ioc2 |  | Debian 9 | HP  |


## IOC migration status

| iocN | PORT | EXEC                                | R  | M  | Note                                                         |
|------|------|-------------------------------------|----|----|--------------------------------------------------------------|
| 1    | 4072 | /epics/iocs/attn1/st\.cmd           | R  | M  | 9/23/20                                                      |
| 2    | 4074 | /epics/iocs/bpm02/st\.cmd           | R  | M  | 9/25/20 dbGetPdbAddrFromLink macro missing, new .db, bpm03\-sydor from xf04id |
| 3    | 4064 | /epics/iocs/C400/st\.cmd            | R  | M  | 9/23/20                                                      |
| 4    | 4001 | /epics/iocs/calc01/st\.cmd          | R  | M  | Debian calc\-dev defective, local calc used                  |
| 5    | 4055 | /epics/iocs/cam08/st\.cmd           | R  | M  | 9/22/20: X-ray eye                                           |
| 6    | 4081 | /epics/iocs/cam09/st\.cmd           | R  | M  | 9/22/20: WAXS X-ray eye                                      |
| 7    | 4082 | /epics/iocs/cam10/st\.cmd           | R  | M  | 9/22/20: OAV microscope, Light control in CSS (plc1 dio)     |
| 8    | 4061 | /epics/iocs/cam2/st\.cmd            | R  | M  | R3\-8                                                        |
| 9    | 4062 | /epics/iocs/cam3/st\.cmd            | R  | M  | R3\-8                                                        |
| 10   | 4063 | /epics/iocs/cam4/st\.cmd            | R  | M  | R3\-8                                                        |
| 11   | 4067 | /epics/iocs/cam5/st\.cmd            | R  | M  | 9/23/20, Radiation Monitor                                   |
| 12   | 4101 | /epics/iocs/cam\-bpm/st\.cmd        | R  | M  | 9/21/20                                                      |
| 13   | 4102 | /epics/iocs/cam\-dcm/st\.cmd        | R  | M  | 9/21/20, Light on button in CSS needed, Naming fix Mon->Mono |
| 14   | 4105 | /epics/iocs/cam\-fs1/st\.cmd        | R  | M  | 9/21/20, Insert/Retract DIO feature                          |
| 15   | 4106 | /epics/iocs/cam\-fs2/st\.cmd        | R  | M  | 9/21/20, Insert/Retract DIO feature                          |
| 16   | 4104 | /epics/iocs/cam\-pbs/st\.cmd        | R  | M  | 9/21/20                                                      |
| 17   | 4103 | /epics/iocs/cam\-wbs/st\.cmd        | R  | M  | 9/21/20                                                      |
| 18   | 4059 | /epics/iocs/det01/st\.cmd           | \- | \- | COMPLETED as Eiger1M                                         |
| 19   | 4069 | /epics/iocs/det02\_AD\-3\-7/st\.cmd | \- | \- | Not needed                                                   |
| 20   | 4069 | /epics/iocs/det02/st\.cmd           | \- | \- | COMPLETED Eiger4M                                            |
| 21   | 4080 | /epics/iocs/det03/st\.cmd           | \- | \- | COMPLETED Eiger 500k                                         |
| 22   | 6001 | /epics/iocs/dlm4000/st\.cmd         |    |    | Yokogawa drive (6), SAX table/pipe. APSshare missing         |
| 23   | 4073 | /epics/iocs/env01/st\.cmd           | R  | M  | 9/24/20, Lakeshore 336                                       |
| 24   | 4077 | /epics/iocs/fb1/st\.cmd             | -  | -  | 9/25/20, Not needed. Backed in gitlab/mercurial              |
| 25   | 4058 | /epics/iocs/mc01/st\.cmd            | R  | M  | 8/24/2020                                                    |
| 26   | 4050 | /epics/iocs/mc02/st\.cmd            | R  | M  | 8/24/2020                                                    |
| 27   | 4060 | /epics/iocs/mc03/st\.cmd            | R  | M  | 8/24/2020                                                    |
| 28   | 4052 | /epics/iocs/mc04/st\.cmd            | R  | M  | 8/24/2020                                                    |
| 29   | 4053 | /epics/iocs/mc05/st\.cmd            | R  | M  | 9/23/2020, Radiation Monitor                                 |
| 30   | 4054 | /epics/iocs/mc06/st\.cmd            | R  | M  | 8/24/2020                                                    |
| 31   | 4066 | /epics/iocs/mc07/st\.cmd            | R  | M  | 8/24/2020                                                    |
| 32   | 4056 | /epics/iocs/mc08/st\.cmd            | R  | M  | 8/24/2020                                                    |
| 33   | 4070 | /epics/iocs/mc09/st\.cmd            | R  | M  | 9/2/2020                                                     |
| 34   | 4078 | /epics/iocs/mc11/st\.cmd            | R  | M  | 9/2/2020                                                     |
| 35   | 4057 | /epics/iocs/mc12/st\.cmd            | R  | M  | SmarAct 9/11/20                                              |
| 36   | 4079 | /epics/iocs/mc13/st\.cmd            | \- | \- | SmarAct \- no hardware N/A                                   |
| 37   | 4065 | /epics/iocs/mc14/st\.cmd            | R  | M  | SmarAct 9/11/20                                              |
| 38   | 4076 | /epics/iocs/mc15/st\.cmd            | R  | M  | SmarAct 9/16/20                                              |
| 39   | 4122 | /epics/iocs/mc16/st\.cmd            |    |    | SmarAct 10/20 planned with beam                              |
| 40   | 4123 | /epics/iocs/mc17/st\.cmd            | \- | \- | SmarAct \- no hardware N/A                                   |
| 41   | 4085 | /epics/iocs/smarpod/st\.cmd         |    |    | ???                                                          |
| 42   | 6002 | /epics/iocs/syringepump/st\.cmd     | R  | M  | 9/23/20, Use EPICS R3-9                                      |
| 43   | 4071 | /epics/iocs/trigger/st\.cmd         | R  | M  | 9/25/20                                |
| 44   | 4051 | /epics/iocs/va\-1/st\.cmd           | R  | M  | 9/25/20                                                             |
| 45   | 4075 | /epics/iocs/vmemon1/st\.cmd         |    |    | CHANGE PVs\!\!\!, vmemon adandoned\-> wienercarate \(4idi1\) |
| 46   | 4068 | /epics/iocs/zebra/st\.cmd           | R  | M  | COMPLETED zebra2 \(5idi1,5iddi1nmd\)                         |
| 47   | 6005 | /epics/iocs/cam\-bfly1/st\.cmd      | N  | M  | Stopped                                                      |
| 48   | 6005 | /epics/iocs/cam\-bfly2/st\.cmd      | R  | M  | Stopped: Might be a temporary camera                         |
| 49   | 6004 | /epics/iocs/cam\-bfly3/st\.cmd      | R  | M  |                                                              |
| 50   | 6008 | /epics/iocs/Eiger1M/st\.cmd         | R  | M  |                                                              |
| 51   | 6009 | /epics/iocs/Eiger4M/st\.cmd         | R  | M  |                                                              |
| 52   | 6007 | /epics/iocs/Eiger500K/st\.cmd       | R  | M  |                                                              |
| 53   | 6003 | /epics/iocs/ioLogik/st\.cmd         | R  | M  |                                                              |



## Migration schedule

* xf11idb-ioc2 in place upgrade Debian8->Debian9
* Eiger detectors
* ioLogik
* cameras
* motion
* feedback
* VME

## Legend
* R = Registered
* M = Migrated
