# Week 5A

## Task 1

### a

The region $H<E$ in the phase space is a hyperellipsoid with semiaxes
$\sqrt{2mE}, \sqrt{2mE}, \sqrt{2E/m\omega^2}, \sqrt{2E/m\omega^2}$.
Therefore, the volume is

```math
V(E) = \frac{\pi^2}{\Gamma(3)}\,2mE\,\frac{2E}{m\omega^2}
=2\pi^2\frac{E^2}{\omega^2}.
```

The density of states is

```math
g(E) = \frac1h\frac{\mathrm dV}{\mathrm dE} = \frac{4\pi^2E}{h\omega^2}.
```

### b

```math
Z(\beta)=\int_0^\infty g(E)\,\mathrm e^{-\beta E}\,\mathrm dE
=\frac{4\pi^2}{\beta^2h\omega^2}.
```

### c

First consider $\lambda>0$.
After some calculation, for any fixed $E,p_x,p_y$, the condition $H<E$ reduces to

```math
x^2+y^2<\frac{m\omega^2}{4\lambda}\left(-1+\sqrt{1+\frac{16\lambda}{m^2\omega^4}\left(E-\frac{p_x^2+p_y^2}{2m}\right)}\right).
```

This means that the cross section of the region $H<E$ on the $xy$ plane is a circle with area $\pi$ times the expression on the RHS of the above.
Therefore, the total volume of the region is

```math
V(E)=\int_0^{\sqrt{2mE}}2\pi p\,\mathrm dp\,\pi\frac{m\omega^2}{4\lambda}\left(-1+\sqrt{1+\frac{16\lambda}{m^2\omega^4}\left(E-\frac{p^2}{2m}\right)}\right)
=\frac{\pi^2m^4\omega^6}{48\lambda^2}\left(\left(1+2\eta\right)\left(-1+\sqrt{1+2\eta}\right)-\eta\right),
```

where $\eta:=8\lambda E/m^2\omega^4$ is defined for brevity.
The density of states is then

```math
g(E)=\frac1h\frac{\mathrm dV}{\mathrm dE}=\frac{\pi^2m^2\omega^2}{2h\lambda}\left(-1+\sqrt{1+2\eta}\right).
```

One may check that the previous results can be recovered by the limit $\lambda\to0$.

For $\lambda<0$, the density of states will diverge.

## Task 2

### a

```math
T_1=\frac12m_1L_1^2\dot\theta_1^2,\qquad U_1=-m_1gL_1\cos\theta_1,
\qquad U_2=-m_2g\left(L_1\cos\theta_1+L_2\cos\theta_2\right),
```

```math
T_2=\frac12m_2\left(L_1^2\dot\theta_1^2+L_2^2\dot\theta_2^2+2L_1L_2\dot\theta_1\dot\theta_2\cos(\theta_1-\theta_2)\right),
```

```math
L=\frac12\left(m_1+m_2\right)L_1^2\dot\theta_1^2+\frac12m_2L_2^2\dot\theta_2^2+m_2L_1L_2\dot\theta_1\dot\theta_2\cos(\theta_1-\theta_2)+\left(m_1+m_2\right)gL_1\cos\theta_1+m_2gL_2\cos\theta_2.
```

### b

```math
p_1=\frac{\partial L}{\partial\dot\theta_1}=\left(m_1+m_2\right)L_1^2\dot\theta_1+m_2L_1L_2\dot\theta_2\cos(\theta_1-\theta_2),
```

```math
p_2=\frac{\partial L}{\partial\dot\theta_2}=m_2L_2^2\dot\theta_2+m_2L_1L_2\dot\theta_1\cos(\theta_1-\theta_2).
```

```math
H=\dot\theta_1 p_1+\dot\theta_2 p_2-L
=\frac{\frac12m_2L_2^2p_1^2+\frac12\left(m_1+m_2\right)L_1^2p_2^2-m_2L_1L_2p_1p_2\cos(\theta_1-\theta_2)}{m_2\left(m_1+m_2-m_2\cos^2(\theta_1-\theta_2)\right)L_1^2L_2^2}
-\left(m_1+m_2\right)gL_1\cos\theta_1-m_2gL_2\cos\theta_2
```

### c

See `task2.py`.

### d

See `task2.py`.
