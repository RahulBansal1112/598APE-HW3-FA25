# 598APE-HW3

This repository contains code for homework 3 of 598APE.

This assignment is relatively simple in comparison to HW1 and HW2 to ensure you have enough time to work on the course project.

In particular, this repository implements a 2D Ising model Monte Carlo simulator (with Metropolis–Hastings algorithm) on an L×L lattice with periodic boundary conditions.

## Optimization Branches

### [metropolisHastingsStep](https://github.com/RahulBansal1112/598APE-HW3-FA25/tree/metropolisHastingsStep)  
This corresponds to the optimization described in **Section 2.1** of our paper.

### [parallelization](https://github.com/RahulBansal1112/598APE-HW3-FA25/tree/parallelization)  
This corresponds to the optimization described in **Section 2.2** of our paper.

### [modulus](https://github.com/RahulBansal1112/598APE-HW3-FA25/tree/modulus)  
This corresponds to the optimization described in **Section 2.3** of our paper.

---

To compile the program run:
```bash
make -j
```

To clean existing build artifacts run:
```bash
make clean
```

This program assumes the following are installed on your machine:
* A working C compiler (gcc is assumed in the Makefile)
* make
* ImageMagick `convert` for PNG output

Usage (after compiling):
```bash
./main.exe <L> <temperature> <steps>
```

In particular, consider speeding up simple run like the following (which runs ~5 seconds on my local laptop under the default setup):
```bash
./main.exe 100 2.269 100000
```

Exact bitwise reproducibility is not required; sanity checks on energy/magnetization bounds must pass. In addition, at the critical temperature (T ≈ 2.269) the energy per spin should approach -1.414 in equilibrium.
