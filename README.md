## Validation of the gem5 Simulator for x86 Architectures

This repository contains modified gem5 source code and configurational changes needed to model an Intel Haswell processor
as referred in [1].
The baseline gem5 source used in this work is commit 1991ff3bb26f89d869a098db33.
Commit ids  684dc51ff3359ddc334873f7c1d and 48af1f007575ccb36dfa04b187f6229 correspond to most of
the source code changes in the simulator.
Commit f86d8bc062f554ffaf06ef56d refers to the baseline configurational changes (base_config) done to model an Intel Haswell core and commit 7c78409cafdd61ef29aeb09e shows the configurational tweaks (calib_config) needed to improve the accuracy that we came up with following a source code analysis and further experiments.

Some of the configuration parameters like (cache sizes) are set through the command line when running gem5.
The command used to run benchmarks is following:

```sh
build/X86/gem5.opt configs/example/se.py --cpu-type=detailed --cpu-clock=3.4GHz --sys-clock=2GHz --caches --l1d_size='32kB' --l1i_size='32kB' --l1i_assoc='8' --l1d_assoc='8' --l2cache --l2_size='256kB' --l2_assoc='8' --l3cache --l3_size='8MB' --l3_assoc='16'  --mem-type=SimpleMemory --mem-size='2GB' -c [benchmark binary and arguments]
```

Please, refer to [1] for details of this work.

## Reference
```
[1] Validation of the gem5 Simulator for x86 Architectures, Ayaz Akram, and Lina Sawalha, In IEEE/ACM Performance Modeling, Benchmarking and Simulation of High Performance Computer Systems (PMBS) in conjunction with Supercomputing Conference (SC19), November 2019.
```
