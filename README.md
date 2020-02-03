## Validation of the gem5 Simulator for x86 Architectures

This repository contains modified gem5 source code and configurational changes needed to model an Intel Haswell processor
as referred in [1].
The baseline gem5 source used in this work is commit 1991ff3bb26f89d869a098db33.
Commit ids  684dc51ff3359ddc334873f7c1d and 48af1f007575ccb36dfa04b187f6229 correspond to most of
the source code changes in the simulator.
Commit f86d8bc062f554ffaf06ef56d refers to the baseline configurational changes (base_config) done to model an Intel Haswell core and commit 7c78409cafdd61ef29aeb09e shows the configurational tweaks (calib_config) needed to improve the accuracy that we came up with following a source code analysis and further experiments.

Please, refer to [1] for details of this work.

## Reference
```
[1] Validation of the gem5 Simulator for x86 Architectures, Ayaz Akram, and Lina Sawalha, In IEEE/ACM Performance Modeling, Benchmarking and Simulation of High Performance Computer Systems (PMBS) in conjunction with Supercomputing Conference (SC19), November 2019.
```
