# Workstation system: quetta

## hosts

* quetta.phys.s.u-tokyo.ac.jp (login server ログインサーバ)
  * CPU: Intel(R) Xeon(R) E-2334 CPU @ 3.40GHz x 1
  * Total Number of Cores: 4
  * Total Memory: 32738508 kB
  * only accepts SSH from inside UTokyo / 東大内からのみSSH可
  * only accepts public key authentication / 公開鍵認証のみ
* quetta-c01, quetta-c02, quetta-c03, quetta-c04, quetta-c05, quetta-c06 (CPU server)
  * 1台あたり
    * CPU: Intel(R) Xeon(R) Platinum 8358 CPU @ 2.60GHz x 2
    * Total Number of Physical Cores: 64
    * Total Memory: 500 GB
* quetta-g01 (GPGPU server)
  * CPU: AMD EPYC 7543 32-Core Processor x 2
  * Total Number of Physical Cores: 64
  * Total Memory: 1000 GB
  * NVIDIA A100 x 8
* filesystem
  * /home - SSD 18 TB
  * /work - HD 60 TB
  * spare: SSD 18TB, HD 60TB

## Compilers, Libraries, etc / コンパイラ、ライブラリ、他

* Ubuntu 22.04
* GNU Compiler 11.3 (gcc, g++, gfortran)
* Intel(R) oneAPI Compiler 2023.1 (icx, icpx, ifx)
* openmpi 4.1.0 (mpicc, mpicxx, mpif90)
  * デフォルトでは mpi* は Intel compiler を呼び出します
  * GNU compiler を使いたい場合は ```source /opt/materiapps/gcc/env.sh``` を実行してください
* OpenBLAS, MKL
* cuda 12.0
* cmake 3.26.4
* python 3.11.4 including numpy, scipy, matplotlib, etc

## Job Scheduler

* Slurm
