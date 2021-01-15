# RecCaster deployment

| Beamline | CHX        |
|----------|------------|
| Date     | 12/28/2020 |
| Author   | K. Gofron  |

# 11ID RecCaster

|    | xf11ida-ioc1:/epics/iocs           | Status                   | RecCaster |
|----|------------------------------------|--------------------------|-----------|
| 1  | /etc/init.d/softioc-bi-bpm         | Running                  |           |
| 2  | /etc/init.d/softioc-cam-bpm        | Stopped.  Not registered |           |
| 3  | /etc/init.d/softioc-cam-dcm        | Stopped.  Not registered |           |
| 4  | /etc/init.d/softioc-cam-fs1        | Stopped.  Not registered |           |
| 5  | /etc/init.d/softioc-cam-fs2        | Stopped.  Not registered |           |
| 6  | /etc/init.d/softioc-cam-pbs        | Stopped.  Not registered |           |
| 7  | /etc/init.d/softioc-cam-wbs        | Stopped.  Not registered |           |
| 8  | /etc/init.d/softioc-cryo           | Running                  | Y         |
| 9  | /etc/init.d/softioc-dg645          | Running                  | Y         |
| 10 | /etc/init.d/softioc-mc1            | Running                  | Y         |
| 11 | /etc/init.d/softioc-mc2            | Running                  | Y         |
| 12 | /etc/init.d/softioc-mc3            | Running                  | Y         |
| 13 | /etc/init.d/softioc-mc4            | Running                  | Y         |
| 14 | /etc/init.d/softioc-mc5            | Running                  | Y         |
| 15 | /etc/init.d/softioc-misc           | Running                  | Y         |
| 16 | /etc/init.d/softioc-omega_i_series | Running                  |           |
| 17 | /etc/init.d/softioc-pi-motors      | Running                  | Y         |
| 18 | /etc/init.d/softioc-plc1           | Running                  |           |
| 19 | /etc/init.d/softioc-recsyncIOC     | Running                  | Y         |
| 20 | /etc/init.d/softioc-va-1           | Running                  |           |

|    | xf11idb-ioc1                     | Status                    | RecCaster |
|----|----------------------------------|---------------------------|-----------|
| 1  | /etc/init.d/softioc-attn1        | Stopped.  Not registered  |           |
| 2  | /etc/init.d/softioc-bpm02        | Stopped.  Not registered  |           |
| 3  | /etc/init.d/softioc-C400         | Stopped.  Not registered  |           |
| 4  | /etc/init.d/softioc-calc01       | Stopped.  Not registered  |           |
| 5  | /etc/init.d/softioc-cam08        | Stopped.  Not registered  |           |
| 6  | /etc/init.d/softioc-cam09        | Stopped.  Not registered  |           |
| 7  | /etc/init.d/softioc-cam10        | Stopped.  Not registered  |           |
| 8  | /etc/init.d/softioc-cam2         | Stopped.  Not registered  |           |
| 9  | /etc/init.d/softioc-cam3         | Stopped.  Not registered  |           |
| 10 | /etc/init.d/softioc-cam4         | Stopped.  Not registered  |           |
| 11 | /etc/init.d/softioc-cam5         | Stopped.  Not registered  |           |
| 12 | /etc/init.d/softioc-cam-bpm      | Stopped.  Not registered  |           |
| 13 | /etc/init.d/softioc-cam-dcm      | Stopped.  Not registered  |           |
| 14 | /etc/init.d/softioc-cam-fs1      | Stopped.  Not registered  |           |
| 15 | /etc/init.d/softioc-cam-fs2      | Stopped.  Not registered  |           |
| 16 | /etc/init.d/softioc-cam-pbs      | Stopped.  Not registered  |           |
| 17 | /etc/init.d/softioc-cam-wbs      | Stopped.  Not registered  |           |
| 18 | /etc/init.d/softioc-det01        | Stopped.  Not registered  |           |
| 19 | /etc/init.d/softioc-det02        | Stopped.  Not registered  |           |
| 20 | /etc/init.d/softioc-det02_AD-3-7 | Stopped.  Not registered  |           |
| 21 | /etc/init.d/softioc-det03        | Stopped.  Not registered  |           |
| 22 | /etc/init.d/softioc-dlm4000      | Running                   |           |
| 23 | /etc/init.d/softioc-Eiger1M      | Stopped.  Not registered  |           |
| 24 | /etc/init.d/softioc-Eiger4M      | Stopped.  Not registered  |           |
| 25 | /etc/init.d/softioc-Eiger500K    | Stopped.  Not registered  |           |
| 26 | /etc/init.d/softioc-env01        | Stopped.  Not registered  |           |
| 27 | /etc/init.d/softioc-fb1          | Stopped.  Not registered  |           |
| 28 | /etc/init.d/softioc-mc01         | Stopped.  Not registered  |           |
| 29 | /etc/init.d/softioc-mc02         | Stopped.  Not registered  |           |
| 30 | /etc/init.d/softioc-mc03         | Stopped.  Not registered  |           |
| 31 | /etc/init.d/softioc-mc04         | Stopped.  Not registered  |           |
| 32 | /etc/init.d/softioc-mc05         | Stopped.  Not registered  |           |
| 33 | /etc/init.d/softioc-mc06         | Stopped.  Not registered  |           |
| 34 | /etc/init.d/softioc-mc07         | Stopped.  Not registered  |           |
| 35 | /etc/init.d/softioc-mc08         | Stopped.  Not registered  |           |
| 36 | /etc/init.d/softioc-mc09         | Stopped.  Not registered  |           |
| 37 | /etc/init.d/softioc-mc11         | Stopped.  Not registered  |           |
| 38 | /etc/init.d/softioc-mc12         | Stopped.  Not registered  |           |
| 39 | /etc/init.d/softioc-mc13         | Stopped.  Not registered  |           |
| 40 | /etc/init.d/softioc-mc14         | Stopped.  Not registered  |           |
| 41 | /etc/init.d/softioc-mc15         | Stopped.  Not registered  |           |
| 42 | /etc/init.d/softioc-mc16         | Stopped.  Not registered  |           |
| 43 | /etc/init.d/softioc-mc17         | Stopped.  Not registered  |           |
| 44 | /etc/init.d/softioc-smarpod      | Stopped                   |           |
| 45 | /etc/init.d/softioc-syringepump  | Stopped.  Not registered  |           |
| 46 | /etc/init.d/softioc-trigger      | Stopped.  Not registered  |           |
| 47 | /etc/init.d/softioc-va-1         | Stopped.  Not registered  |           |
| 48 | /etc/init.d/softioc-vmemon1      | Running                   |           |
| 49 | /etc/init.d/softioc-zebra        | Stopped.  Not registered  |           |

|    | xf11idb-ioc2                    | Status                   | RecCaster |
|----|---------------------------------|--------------------------|-----------|
| 1  | /etc/init.d/softioc-attn1       | Running                  | Y         |
| 2  | /etc/init.d/softioc-bpm02       | Running                  | Y         |
| 3  | /etc/init.d/softioc-C400        | Running                  | Y         |
| 4  | /etc/init.d/softioc-calc01      | Running                  | Y         |
| 5  | /etc/init.d/softioc-cam10       | Running                  |           |
| 6  | /etc/init.d/softioc-cam2        | Running                  |           |
| 7  | /etc/init.d/softioc-cam3        | Running                  |           |
| 8  | /etc/init.d/softioc-cam4        | Running                  |           |
| 9  | /etc/init.d/softioc-cam5        | Running                  |           |
| 10 | /etc/init.d/softioc-cam-bfly1   | Stopped.  Not registered |           |
| 11 | /etc/init.d/softioc-cam-bfly2   | Stopped                  |           |
| 12 | /etc/init.d/softioc-cam-bfly3   | Running                  |           |
| 13 | /etc/init.d/softioc-cam-bpm     | Running                  |           |
| 14 | /etc/init.d/softioc-cam-dcm     | Running                  |           |
| 15 | /etc/init.d/softioc-cam-fs1     | Running                  |           |
| 16 | /etc/init.d/softioc-cam-fs2     | Running                  |           |
| 17 | /etc/init.d/softioc-cam-pbs     | Running                  |           |
| 18 | /etc/init.d/softioc-cam-WAXS    | Running                  |           |
| 19 | /etc/init.d/softioc-cam-wbs     | Running                  |           |
| 20 | /etc/init.d/softioc-cam-XrayEye | Running                  |           |
| 21 | /etc/init.d/softioc-Eiger1M     | Running                  |           |
| 22 | /etc/init.d/softioc-Eiger4M     | Running                  |           |
| 23 | /etc/init.d/softioc-Eiger500K   | Running                  |           |
| 24 | /etc/init.d/softioc-env01       | Running                  | Y         |
| 25 | /etc/init.d/softioc-ioLogik     | Running                  | Y         |
| 26 | /etc/init.d/softioc-mc01        | Running                  | Y         |
| 27 | /etc/init.d/softioc-mc02        | Running                  | Y         |
| 28 | /etc/init.d/softioc-mc03        | Running                  | Y         |
| 29 | /etc/init.d/softioc-mc04        | Running                  | Y         |
| 30 | /etc/init.d/softioc-mc05        | Running                  | Y         |
| 31 | /etc/init.d/softioc-mc06        | Running                  | Y         |
| 32 | /etc/init.d/softioc-mc07        | Running                  | Y         |
| 33 | /etc/init.d/softioc-mc08        | Running                  | Y         |
| 34 | /etc/init.d/softioc-mc09        | Running                  | Y         |
| 35 | /etc/init.d/softioc-mc11        | Running                  | Y         |
| 36 | /etc/init.d/softioc-mc12        | Running                  | Y         |
| 37 | /etc/init.d/softioc-mc14        | Running                  | Y         |
| 38 | /etc/init.d/softioc-mc15        | Running                  | Y         |
| 39 | /etc/init.d/softioc-mc16        | Running                  | Y         |
| 40 | /etc/init.d/softioc-syringepump | Running                  | Y         |
| 41 | /etc/init.d/softioc-trigger     | Running                  | Y         |
| 42 | /etc/init.d/softioc-va-1        | Running                  | Y*        |
| 43 | /etc/init.d/softioc-zebra       | Running                  | Y         |