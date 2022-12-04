# LUE_small

LUE (Laguerre Unitary Ensemble) iid samples for sizes 1000 to 10000

This repository contains Laguerre-$\alpha$ Unitary Ensemble (LUE-$\alpha$) iid (independent and identically distributed) samples for $N=1000, 5000, 10000$ particles. More precisely, consider the LUE-$\alpha$ distribution on ordered tuples of $N$ positive real numbers $(x_1 < \dots < x_N)$. That is, consider the probability measure

$$P(\lambda_1, \dots, \lambda_N)d \lambda_1 \dots d \lambda_N = \prod_{1 \leq i < j \leq N} (\lambda_i - \lambda_j)^2 \prod_{1 \leq i \leq N} \lambda_i^{\alpha-1} e^{-\lambda_i} d \lambda_i$$

where $\alpha > 0$ (notice the somewhat less standard $\alpha$ convention we use for LUE).

Iid samples from this distribution are given as follows:
- each file is a ```.tar.gz``` archive of a text file
- each line in each text file is an independent sample, starting from $\lambda_1$ (first column)
- the number of samples is given by ```N * num_samples = 1 000 000```
- a file named e.g. ```LUE_N_5000_alpha_6.75.txt``` has $N=5000, \alpha = 6.75$, and hence 2000 lines.
