# Masterclass 2022 - software

In this repository we report a brief guide on how to install the software needed for PLUMED Masterclass 2022.
Notice that different masterclass might require different software versions.
Our recommendation is to use conda. Unfortunately we can only provide precompiled conda packages for x64 architecture, Linux and MacOS.
This means that if you want to run the exercise on a different architecture you should install the software on your own.

A basic installation with plumed 2.7.3 and all contributed modules enabled, plus gromacs 2020.6, both compiled with MPI, can be done with the following commands:
```
conda create --name plumed-masterclass-2022
source activate plumed-masterclass-2022
# install some basic analysis tool and the default plumed version
conda install -c conda-forge plumed py-plumed numpy pandas matplotlib notebook mdtraj mdanalysis git
# install plumed 2.7.3 with MPI and all modules enabled
conda install --strict-channel-priority -c plumed/label/masterclass-2022 -c conda-forge plumed
# install gromacs 2020.6 with MPI and patched with PLUMED
conda install --strict-channel-priority -c plumed/label/masterclass-2022 -c conda-forge gromacs
```

Conda will install a number of packages.
On MacOS, for instance, you should see something similar to this:
```
  boost-cpp          conda-forge/osx-64::boost-cpp-1.77.0-hf3dc895_1
  bzip2              conda-forge/osx-64::bzip2-1.0.8-h0d85af4_4
  fftw               conda-forge/osx-64::fftw-3.3.10-nompi_hf082fe4_102
  gawk               conda-forge/osx-64::gawk-5.1.0-h8a989fb_0
  gettext            conda-forge/osx-64::gettext-0.19.8.1-hd1a6beb_1008
  gromacs            plumed/label/masterclass-2022/osx-64::gromacs-2020.6-h75233e6_0
  gsl                conda-forge/osx-64::gsl-2.7-h93259b0_0
  icu                conda-forge/osx-64::icu-69.1-he49afe7_0
  libblas            conda-forge/osx-64::libblas-3.9.0-13_osx64_openblas
  libcblas           conda-forge/osx-64::libcblas-3.9.0-13_osx64_openblas
  libcxx             conda-forge/osx-64::libcxx-12.0.1-habf9029_1
  libffi             conda-forge/osx-64::libffi-3.4.2-h0d85af4_5
  libgfortran        conda-forge/osx-64::libgfortran-5.0.0-9_3_0_h6c81a4c_23
  libgfortran5       conda-forge/osx-64::libgfortran5-9.3.0-h6c81a4c_23
  libhwloc           conda-forge/osx-64::libhwloc-1.11.13-hc10311c_0
  libiconv           conda-forge/osx-64::libiconv-1.16-haf1e3a3_0
  liblapack          conda-forge/osx-64::liblapack-3.9.0-13_osx64_openblas
  libopenblas        conda-forge/osx-64::libopenblas-0.3.18-openmp_h3351f45_0
  libxml2            conda-forge/osx-64::libxml2-2.9.12-h7e28ab6_1
  libzlib            conda-forge/osx-64::libzlib-1.2.11-h9173be1_1013
  llvm-openmp        conda-forge/osx-64::llvm-openmp-12.0.1-hda6cdc1_1
  lz4-c              conda-forge/osx-64::lz4-c-1.9.3-he49afe7_1
  mpi                conda-forge/osx-64::mpi-1.0-openmpi
  ncurses            conda-forge/osx-64::ncurses-6.3-he49afe7_0
  openmpi            conda-forge/osx-64::openmpi-4.1.2-hd3cd54c_0
  plumed             plumed/label/masterclass-2022/osx-64::plumed-2.7.3-h75233e6_0
  readline           conda-forge/osx-64::readline-8.1-h05e3726_0
  xdrfile            conda-forge/osx-64::xdrfile-1.1.4-h0d85af4_1
  xz                 conda-forge/osx-64::xz-5.2.5-haf1e3a3_1
  zlib               conda-forge/osx-64::zlib-1.2.11-h9173be1_1013
  zstd               conda-forge/osx-64::zstd-1.5.2-h582d3a0_0
```
 Make sure that `gromacs` and `plumed` packages are installed from `plumed/label/masterclass-2022`.
