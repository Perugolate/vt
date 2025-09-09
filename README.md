# contents

 - [connect to cluster](#connect-to-cluster)
 - [install `conda`](#install-conda)
 - [create a conda environment](#create-a-conda-environment)
 - [using the conda environment](#using-the-conda-environment)
   - [](#)
   - [](#)
   - [](#)

## connect to cluster

```bash
# replace "CROP_DIVERSITY_USERNAME" with your actual cluster username
ssh CROP_DIVERSITY_USERNAME@gruffalo.cropdiversity.ac.uk
```

## install `conda`

You only need to do this step once (the very first time you use conda on the cluster).

`conda` is a package manager that simplifies the installation of software and its dependencies. There is a script `install-bioconda` that has been created by the  system administrator to ensure that `conda` is installed to the fast SSD storage array (rather than the default location).

Simply run the following command:

```bash
install-bioconda
```

Your shell needs to be reloaded to recognize the `conda` command. You can do this by closing and reopening your terminal session. Either type `exit` and press Enter or use the shortcut <kbd>Ctrl</kbd> + <kbd>D</kbd>.

## create a conda environment

I strongly recommend that you create a separate conda environment for each software package you want to use. This allows you to manage different versions of software and their dependencies without conflicts.

To create a conda environment named `medaka_v2.1.1` (containing `medaka` version 2.1.1), use the following command:

```bash
conda create -n medaka_v2.1.1 medaka=2.1.1
```

You will be prompted to confirm the installation of the package and its dependencies. Type `y` and press Enter to proceed.


## create working directory


Doublecheck you are connected to the cluster by printing the hostname:

```bash
hostname
```

This should return:

```console
gruffalo.hpc.hutton.ac.uk
```


Doublecheck you are in the right place by printing the current directory:

```bash
pwd
```



















## using the conda environment

To use the conda environment you created, you need to activate it. This sets up your shell to use the software and packages installed in that environment.

To activate the `medaka_v2.1.1` environment inside your scripts, include the following command:

```bash
conda activate medaka_v2.1.1
```



