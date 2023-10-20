# turing-instructions

WPI maintains a HPC cluster for teaching 
and research purposes, known as Turing.  It has significant 
capabilities, but is a shared resource and is still limited in what it 
can accomodate.

This readme contains some essential information to help you get started! Please feel free to express your feedback on these instructions by creating an issue on this repo.

## Login node, Compute node, SLURM Overview:

As a general overview: Turing is a linux-based system, running Ubuntu 
20.04, with jobs managed by the SLURM scheduler.  In general, you will 
use ssh to connect to `turing.wpi.edu`, which will connect you to one of 
the login nodes.  These do not have GPUs or the power to do 'real work', 
but instead are used for managing jobs running on its many compute 
nodes.  From there, you can work with SLURM, giving it jobs to be run on 
the hardware with GPUs.  Note that all GPU access is mediated by SLURM 
-- you can't use any GPU time without it giving it to you, but that also 
guarantees that nobody else will attempt to use that GPU while your code 
is using it.

For most normal work, this is done by writing a short shell script, 
which will describe the resources required to run the job, load the 
software modules (primarily: cuda toolkit and python environment), and 
then run your code.

## Instructions for getting started:

1. ssh to cluster 

2. load all the modules required such as python, cuda etc 

3. source the pip venv which has all the required libraries. Alternatively you can use conda to install/manage the packages.

4. submits the job to slurm via shell script

Here is the [video tutorial](https://drive.google.com/file/d/11a7mzO46QTmzTR4lz_ioEXq8I8VPTs8v/view?usp=sharing) from Ramana outlining the same. Accompanying files for the [video tutorial](https://github.com/saikrn112/turing_cluster) are hosted here.

### Related video tutorials:

- [Terminal tutorial](https://www.youtube.com/watch?v=vhZLTp6N4XA&ab_channel=ProgrammingKnowledge)

- [SSH tutorial](https://www.youtube.com/watch?v=5Fcf-8LPvws&ab_channel=thenewboston)

- [Virtual env tutorial](https://youtu.be/Kg1Yvry_Ydk?t=515)

### Turing documentation:

[Turing Basic User Guide](https://arc.wpi.edu/turing-basic-user-guide/)

[WPI HPC Documentation](https://arc.wpi.edu/cluster-documentation/build/html/intro.html)



*Acknowledgements:*
*Thanks to Ramana and James for providing this content.*