# Li–Liu’s Hypotheses S and R under ERH

This note derives the operator norm criteria for Hypotheses S and R in Jiamin Li and Jianya Liu’s *A Conditional Proof of the Goldbach Conjecture*. It proves $\mathrm R\Rightarrow\mathrm S$ and computes the zero-free width supplied by the paper’s ERH estimate. Deriving either hypothesis from ERH alone remains the missing step.

## Setup

Assume the extended Riemann hypothesis (ERH) in the form of GRH for every primitive Dirichlet $L$-function. In particular, Li–Liu’s local assumption $\mathrm{GRH}(N)$ holds for every even $N$.

For sufficiently large even $N$, let $T_N$ be the compact self-adjoint Hilbert–Schmidt operator constructed from the arithmetic residual. Write $\mathfrak S(N)$ for the Goldbach singular series, $\mu_j$ for the nonzero eigenvalues of $T_N$ counted with multiplicity, and put

$$
\delta_N^2=\frac{\mathfrak S(N)(\log N)^3}{N}.
$$

On each complex slice, Li–Liu’s spectral function is

$$
X_N(q)=\prod_j\left(1-\frac{4\mu_j^2}{\delta_N^2}q(1-q)\right).
$$

For any fixed $N$ and $q$, the deviations of the factors from $1$ are absolutely summable because $\sum_j\mu_j^2<\infty$. If every factor is nonzero, the product is nonzero. Hence every spectral zero comes from a factor. Every quaternion belongs to a complex slice, so the same classification applies to the quaternionic extension.

## Hypothesis R and the operator norm

The roots of the factor indexed by $j$ are

$$
q=\frac12\pm\frac12\sqrt{1-\frac{\delta_N^2}{\mu_j^2}}.
$$

If $|\mu_j|<\delta_N$, both roots have real part $1/2$. Equality gives a double root at $1/2$. If $|\mu_j|>\delta_N$, there are two distinct real roots on opposite sides of $1/2$. By self-adjointness, $\|T_N\|=\sup_j|\mu_j|$, with norm zero when $T_N=0$. Thus

$$
\mathrm R(N)\quad\Longleftrightarrow\quad \|T_N\|\le\delta_N.
$$

## Hypothesis S and the zero-free width

Fix $0<\eta<1/2$. A zero with $\Re q>1-\eta$ can only be the larger member of a real pair. For such a pair, exclusion from that open half-space is equivalent to

$$
\sqrt{1-\frac{\delta_N^2}{\mu_j^2}}\le 1-2\eta
\quad\Longleftrightarrow\quad
|\mu_j|\le\frac{\delta_N}{2\sqrt{\eta(1-\eta)}}.
$$

The same inequality holds automatically for $|\mu_j|\le\delta_N$. Taking the supremum proves

$$
X_N(q)\ne0\ \text{for all }\Re q>1-\eta
\quad\Longleftrightarrow\quad
\|T_N\|\le\frac{\delta_N}{2\sqrt{\eta(1-\eta)}}.
$$

Hypothesis S prescribes a positive function $h(N)\to\infty$ with eventual width

$$
\eta_N=\frac{h(N)^2(\log N)^3}{N\mathfrak S(N)}\le\frac14.
$$

Substituting gives the exact criterion

$$
\mathrm S(N;h)\quad\Longleftrightarrow\quad
\|T_N\|\le\frac{\mathfrak S(N)}{2h(N)\sqrt{1-\eta_N}}.
$$

**Therefore R implies S for every admissible $h$.** Under R every zero has real part $1/2$, whereas S only excludes zeros with real part greater than $1-\eta_N\ge3/4$.

## What ERH gives

Li–Liu’s Theorem 6.2 gives $\|T_N\|\le M_N=C(\log N)^2$ under ERH, with $C$ an absolute constant chosen sufficiently large. For large $N$, $M_N>\delta_N$. The preceding criterion gives a zero-free half-space of width

$$
\eta_N^{\mathrm{ERH}}
=\frac{1-\sqrt{1-\delta_N^2/M_N^2}}{2}
\asymp\frac{\delta_N^2}{M_N^2}
\asymp\frac{\mathfrak S(N)}{N\log N}.
$$

The width in S exceeds this guaranteed width by a factor of order

$$
\frac{\eta_N}{\eta_N^{\mathrm{ERH}}}
\asymp \frac{h(N)^2(\log N)^4}{\mathfrak S(N)^2}
\longrightarrow\infty,
$$

using $\mathfrak S(N)\ll\log\log N$. The paper obtains its ERH bound by estimating the character-average term, the exact diagonal term, and the Beta-model term separately. The remaining problem is to bound their combined residual in operator norm at the threshold for S or R. By the paper’s quadratic-form estimate, either bound would give the weighted binary Goldbach asymptotic for all sufficiently large even $N$.

## Reference

Jiamin Li and Jianya Liu, [*A Conditional Proof of the Goldbach Conjecture*](https://mrc.sdu.edu.cn/__local/6/14/8E/28753731EE31D7635BAF60732C2_0C644604_2CE958.pdf). See §2.4 and Theorems 6.1, 6.2, and 7.1.
