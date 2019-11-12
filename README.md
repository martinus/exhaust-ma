Exhaust-ma is exhaust with some of my optimizations. The interface is exactly the same, but I have optimized the simulation code. IMHO Exhaust-ma currently is the fastest redcode simulator in this universe ;-).

Everybody likes benchmarks, so here they are. All simulators were compiled with the same compiler and compiler options. The commandline was the same. Needless to say, the results were the same too.

* Athlon-XP 2000+, Times in seconds, command line e.g. `time ./exhaust -bkF 4000 -r 1000 fixed.rc fixed.rc`
  ```
    Compiler and options: gcc 3.3.2 -O2 -fomit-frame-pointer -march=athlon-xp
    These options produce faster code than -O2 or -O3

                         pmars-0.9.2 exhaust-1.9 exhaust-ma      W   L   T
       Fixed vs    Fixed       4,775       3,981      3,026    277 324 399
      Jaguar vs    Fixed       6,222       5,523      4,059    248 219 533
      Jaguar vs   Jaguar       8,382       7,795      5,427    125 143 732
     Stalker vs    Fixed       4,523       4,245      2,974    300 525 175
     Stalker vs   Jaguar       4,806       4,649      3,255    366 407 227
     Stalker vs  Stalker       3,850       3,759      2,630    470 458  72
    nPaperII vs    Fixed       7,102       5,976      4,634    215 173 612
    nPaperII vs   Jaguar       8,815       7,804      5,781    142  90 768
    nPaperII vs  Stalker       5,552       5,316      3,825    401 415 184
    nPaperII vs nPaperII       9,672       8,142      5,868     86  94 820
    ----------------------------------------------------------------------
    total:                    63,699      57,190     41,479
    relative time:           100%         89,8%      65,1%
    faster than pmars:         0,0%       11,4%      53,6%
  ```

* AMD K6-2 400, Times in seconds, command line e.g. `time ./exhaust -bkF 4000 -r 1000 fixed.rc fixed.rc`
  ```
    Compiler and options: gcc 2.95.4 -O -fomit-frame-pointer -march=k6
    These options produce faster code than -O2 or -O3

                         pmars-0.9.2 exhaust-1.9 exhaust-ma      W   L   T
       Fixed vs    Fixed       30,51       23,92      20,23    277 324 399
      Jaguar vs    Fixed       28,51       26,80      19,66    248 219 533
      Jaguar vs   Jaguar       32,05       32,94      23,79    125 143 732
     Stalker vs    Fixed       17,89       17,98      13,64    300 525 175
     Stalker vs   Jaguar       18,78       19,34      14,94    366 407 227
     Stalker vs  Stalker       14,83       15,23      12,05    470 458  72
    nPaperII vs    Fixed       42,90       34,11      27,93    215 173 612
    nPaperII vs   Jaguar       41,23       37,50      27,62    142  90 768
    nPaperII vs  Stalker       21,31       21,55      16,78    401 415 184
    nPaperII vs nPaperII       51,48       42,70      32,75     86  94 820
    ----------------------------------------------------------------------
    total:                    299,53      272,07     209,86
    relative time:            100%         90,8%      70,1%
    faster than pmars:          0,0%       10,1%      42,7%
  ```
