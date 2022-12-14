# LUE-small-LFS

LUE (Laguerre Unitary Ensemble) iid samples for sizes 1000, 5000, and 10000

**Note:** This repository uses Git LFS (large file system). To properly use Git with this repository, first install Git LFS from [its website](https://git-lfs.github.com/). Second, to clone the actual files using ```git lfs clone``` and not just a stub of them, see [this tutorial](https://www.atlassian.com/git/tutorials/git-lfs). If you're fine with downloading individual files one by one however, go into ```data``` and click on individual files and then click on Download. This way you can download them, full-size, one at a time.

This repository contains Laguerre $\alpha$ Unitary Ensemble (LUE $\alpha$) iid (independent and identically distributed) samples for $N=1000, 5000, 10000$ particles. More precisely, consider the LUE $\alpha$ distribution on ordered tuples of $N$ positive real numbers $(\lambda_1 < \dots < \lambda_N).$ That is, consider the probability measure

$$P(\lambda_1, \dots, \lambda_N)d \lambda_1 \dots d \lambda_N \propto \prod_{1 \leq i < j \leq N} (\lambda_i - \lambda_j)^2 \prod_{1 \leq i \leq N} \lambda_i^{\alpha-1} e^{-\lambda_i} d \lambda_i$$

where $\alpha > 0$ (notice the somewhat less standard $\alpha$ convention we use for LUE). See [this Wikipedia article](https://en.wikipedia.org/wiki/Complex_Wishart_distribution) for the motivation behind this distribution and how it comes about when studying covariance matrices (see in particular the Eigenvalues section).

Iid samples from this distribution are given as follows:

- each file is a ```.tar.gz``` archive of a text file
- each line in each text file is an independent sample, starting from $\lambda_1$ (first column)
- the number of samples is given by ```N * num_samples = 10 000 000```
- a file named e.g. ```LUE_N_5000_alpha_6.75.txt``` has $N=5000, \alpha = 6.75$, and hence 2000 lines (samples)
- parameter $\alpha$ ranges from 1.00 to 6.75 in increments of 0.25
