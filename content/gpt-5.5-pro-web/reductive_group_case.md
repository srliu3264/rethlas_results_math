+++
title = "Reductive Group Case (gpt-5.5-pro-web)"
date = 2026-05-17
weight = 7
[extra]
math = true
+++

## Statement

Let $G$ be a (not necessarily split) connected reductive group over a field $k$. Let $K$ be an algebraic field extension of $k$. Let

$$\mathbb{X}_ \ast(G) := \mathrm{Hom}_ {k\text{-groups}}(\mathbb{G}_ m, G)$$

$k$-homomorphisms. Let $G_ K$ be the base change of $G$ to $K$. Prove that

$$\mathbb{X}_ \ast(G)/G(k) \to \mathbb{X}_ \ast(G_ K)/G(K)$$

is injective.

## Proof

Let $\lambda,\mu\in \mathbb X_ \ast(G)$. We need to show that if their base changes are $G(K)$-conjugate, then $\lambda$ and $\mu$ are already $G(k)$-conjugate.

Assume

$$\mu_ K=\operatorname{Int}(g)\circ \lambda_ K$$

for some $g\in G(K)$. Since $G$ is of finite type and $K/k$ is algebraic, $g$ is defined over some finite subextension $K_ 0/k$. Thus the transporter below has a point after a finite faithfully flat extension of $k$.

Define the transporter

$$X:=\operatorname{Transp}_ G(\lambda,\mu)=\\{h\in G:\operatorname{Int}(h)\circ\lambda=\mu\\}.$$

This is a closed $k$-subscheme of $G$, and $X(K_ 0)\neq \varnothing$. Let

$$L:=C_ G(\lambda)$$

be the centralizer of the image of $\lambda$. Since $\lambda$ is $k$-defined, $L$ is a $k$-subgroup of $G$. Moreover, $L$ is a Levi subgroup of the $k$-parabolic

$$P_ \lambda=\left\\{x\in G:\lim_ {t\to 0}\lambda(t)x\lambda(t)^{-1}\text{ exists}\right\\}.$$

The group $L$ acts on $X$ on the right by multiplication. If $h\in X$, then

$$hL=\operatorname{Transp}_ G(\lambda,\mu)$$

after any field extension over which $h$ exists. Hence $X$ is a right $L$-torsor over $k$ for the fppf topology.

Now consider the associated $G$-torsor

$$X\times^L G.$$

There is a natural $G$-equivariant isomorphism

$$X\times^L G \longrightarrow G,\qquad [x,a]\longmapsto xa.$$

Therefore the class $[X]\in H^1(k,L)$ maps to the trivial class in $H^1(k,G)$.

We now use the standard fact:

> If $P\subset G$ is a $k$-parabolic subgroup and $L\subset P$ is a $k$-Levi subgroup, then the natural map
>
> $$H^1(k,L)\longrightarrow H^1(k,G)$$
>
> has trivial kernel.

For completeness, here is the proof of that fact. Let $k_ s$ be a separable closure of $k$, and let $\Gamma=\operatorname{Gal}(k_ s/k)$. Suppose a cocycle $z_ \sigma\in Z^1(k,L)$ becomes trivial in $H^1(k,G)$. Then there exists $a\in G(k_ s)$ such that

$$z_ \sigma=a^{-1}\sigma(a).$$

Since $z_ \sigma\in L\subset P$, the point $aP\in (G/P)(k_ s)$ is fixed by $\Gamma$, so $aP\in (G/P)(k)$. For a connected reductive group, the natural map

$$G(k)\longrightarrow (G/P)(k)$$

is surjective: equivalently, $k$-parabolic subgroups of $G$ of the same type are $G(k)$-conjugate. Hence there exists $b\in G(k)$ with

$$aP=bP.$$

Thus $p:=b^{-1}a\in P(k_ s)$, and

$$z_ \sigma=p^{-1}\sigma(p).$$

Let $\pi:P\to L$ be the $k$-homomorphic projection coming from the Levi decomposition $P=L\ltimes R_ u(P)$. Since $z_ \sigma\in L$, applying $\pi$ gives

$$z_ \sigma=\pi(z_ \sigma)=\pi(p)^{-1}\sigma(\pi(p)).$$

So $z_ \sigma$ is already a coboundary in $L$. Therefore $H^1(k,L)\to H^1(k,G)$ has trivial kernel.

Applying this to $L=C_ G(\lambda)$, the torsor $X$ has trivial class in $H^1(k,L)$. Hence $X(k)\neq\varnothing$. Choose $h\in X(k)$. By definition of $X$,

$$\mu=\operatorname{Int}(h)\circ \lambda.$$

Thus $\lambda$ and $\mu$ are $G(k)$-conjugate.

Therefore the map

$$\mathbb X_ \ast(G)/G(k)\longrightarrow \mathbb X_ \ast(G_ K)/G(K)$$

is injective.
