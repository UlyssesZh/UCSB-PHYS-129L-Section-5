# Week 5B

## Task 1

```math
Z=\prod_{k=1}^M\left(1+\mathrm e^{-\beta(k\epsilon-\mu)}\right).
```

## Task 2

### a

There are $N+1$ microstates.
There can be $k$ particles at $E=0$ and $N-k$ particles at $E=\epsilon$,
where $k=0,1,\ldots,N$.

### b

```math
Z_\mathrm{C}=\sum_{k=0}^N\binom{N}{k}\mathrm e^{-\beta k\epsilon}
=\left(1+\mathrm e^{-\beta\epsilon}\right)^N.
```

The probability of finding specific energy $E$ is $\binom{N}{E/\epsilon}\mathrm e^{-\beta E}/Z$
(assuming $E$ is a multiple of $\epsilon$).

### c

```math
\left\langle n_0\right\rangle_\mathrm C=\frac1{Z_\mathrm C}\sum_{k=0}^N\left(N-k\right)\binom{N}{k}\mathrm e^{-\beta k\epsilon}
=\frac N{1+\mathrm e^{-\beta\epsilon}}.
```

```math
\left\langle n_\epsilon\right\rangle_\mathrm C=\frac1{Z_\mathrm C}\sum_{k=0}^Nk\binom{N}{k}\mathrm e^{-\beta k\epsilon}
=\frac N{1+\mathrm e^{\beta\epsilon}}.
```

For plot, see `task2c.py`.

### d

```math
Z=\sum_{k=0}^N\mathrm e^{-\beta k\epsilon}
=\frac{\mathrm e^{\beta\epsilon}-\mathrm e^{-N\beta\epsilon}}{\mathrm e^{\beta\epsilon}-1}.
```

The probability of finding specific energy $E$ is $\mathrm e^{-\beta E}/Z$.

### e

```math
\left\langle n_0\right\rangle=\frac1Z\sum_{k=0}^N\left(N-k\right)\mathrm e^{-\beta k\epsilon}
=N-\frac1{\mathrm e^{\beta\epsilon}-1}+\frac{N+1}{\mathrm e^{(N+1)\beta\epsilon}-1}.
```

```math
\left\langle n_\epsilon\right\rangle=\frac1Z\sum_{k=0}^Nk\mathrm e^{-\beta k\epsilon}
=\frac1{\mathrm e^{\beta\epsilon}-1}-\frac{N+1}{\mathrm e^{(N+1)\beta\epsilon}-1}.
```

### f

```math
\Omega_{\mathrm G}=\sum_{N=0}^\infty\mathrm e^{\beta\mu N}Z
=\frac{1}{\left(\mathrm e^{\beta(\mu-\epsilon)}-1\right)\left(\mathrm e^{\beta\mu}-1\right)}.
```

For the sum to converge, we need $\mu<0$.

### g

The formula is for the average particle number, not for the average particle number in the ground state.

```math
\left\langle N\right\rangle=\frac1{\beta}\frac{\partial}{\partial\mu}\ln\Omega_{\mathrm G}
=\frac{\mathrm e^{\beta(\epsilon-\mu)}\left(1+\mathrm e^{\beta\epsilon}-2\mathrm e^{\beta\mu}\right)}{\left(\mathrm e^{\beta(\mu-\epsilon)}-1\right)^2\left(\mathrm e^{\beta\mu}-1\right)^2}.
```

### h

```math
\left\langle n_0\right\rangle=\frac1{\Omega_{\mathrm G}}\sum_{N=0}^\infty\sum_{k=0}^N\left(N-k\right)\mathrm e^{\beta\mu N}\mathrm e^{-\beta k\epsilon}
=\frac{1}{\mathrm e^{-\beta\mu}-1}.
```

### i

Numerically solve

```math
N=\sum_i\frac1{\mathrm e^{\beta(\epsilon_i-\mu)}-1}
```

to get $\mu$ for any given $N$ and $\beta$.
Take the derivative of both sides of the above equation w.r.t. $\beta$ to get $\mathrm d\mu/\mathrm d\beta$,
which is in turn used to find $\mathrm d\left\langle n_0\right\rangle/\mathrm d\beta$.

See `task2ijk.py`.

### j

See `task2ijk.py`.

### k

See `task2ijk.py`.
