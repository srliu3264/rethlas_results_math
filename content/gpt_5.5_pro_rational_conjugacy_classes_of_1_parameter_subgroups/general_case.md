+++
title = "General Case (gpt-5.5-pro-web)"
date = 2026-05-17
weight = 9
[extra]
math = true
+++

## Statement

Let $G$ be a (not necessarily reductive) smooth connected affine group over a (not necessarily perfect) field $k$. Let $K$ be an algebraic field extension of $k$. Let
$$
\mathbb{X}_ \ast(G) := \operatorname{Hom}_ {k\text{-groups}}(\mathbb{G}_ m, G)
$$
be the $k$-homomorphisms. Let $G_ K$ be the base change of $G$ to $K$. Prove (or disprove with a counterexample) that
$$
\mathbb{X}_ \ast(G)/G(k) \to \mathbb{X}_ \ast(G_ K)/G(K)
$$
is injective. (You can take for granted that this statement is true if $k$ is a perfect field.)

## Proof

The statement is **true**, even slightly more generally: the same proof works for any field extension $K/k$, not just algebraic extensions.

Let
$$
\lambda,\mu\in \mathbb X_ \ast(G)=\operatorname{Hom}_ {k\text{-groups}}(\mathbb G_ m,G)
$$
and suppose that their base changes to $K$ are $G(K)$-conjugate. We prove that $\lambda$ and $\mu$ are already $G(k)$-conjugate.

For a cocharacter $\lambda:\mathbb G_ m\to G$, define the dynamic subgroup
$$
P_ G(\lambda)=\\\{
g\in G:\lim_ {t\to 0}\lambda(t)g\lambda(t)^{-1}\text{ exists}
\\\}.
$$

Also define
$$
C_ G(\lambda)=Z_ G(\lambda(\mathbb G_ m)).
$$

For smooth connected affine $G$, the dynamic theory of Borel--Tits says that $P_ G(\lambda)$ is a smooth connected pseudo-parabolic $k$-subgroup, and that the limit map
$$
\rho:P_ G(\lambda)\to C_ G(\lambda),
\qquad
\rho(g)=\lim_ {t\to 0}\lambda(t)g\lambda(t)^{-1},
$$
is a $k$-homomorphic retraction. In particular,
$$
P_ G(\lambda)=C_ G(\lambda)\ltimes U_ G(\lambda)
$$
for the corresponding contracted unipotent subgroup $U_ G(\lambda)$.

We also use the Borel--Tits rationality theorem in the following form: if $P\subset G$ is a pseudo-parabolic $k$-subgroup of a smooth connected affine $k$-group, then
$$
G(k)\longrightarrow (G/P)(k)
$$
is surjective.

Now we prove the key cohomological lemma.

**Lemma.** For every $k$-cocharacter $\lambda$, the natural map of pointed sets
$$
H^1(k,C_ G(\lambda))\longrightarrow H^1(k,G)
$$
has trivial kernel.

**Proof.** Put
$$
C:=C_ G(\lambda),\qquad P:=P_ G(\lambda).
$$

We have an inclusion $i:C\hookrightarrow P$ and a $k$-homomorphic retraction
$$
\rho:P\to C
$$
with $\rho\circ i=\operatorname{id}_ C$.

For the homogeneous space $G/P$, the standard exact sequence of nonabelian cohomology gives
$$
G(k)\longrightarrow (G/P)(k)\longrightarrow H^1(k,P)\longrightarrow H^1(k,G).
$$

Since $G(k)\to (G/P)(k)$ is surjective, the connecting map $(G/P)(k)\to H^1(k,P)$ has trivial image. Therefore
$$
\ker\bigl(H^1(k,P)\to H^1(k,G)\bigr)=\\{1\\}.
$$

Now let $\alpha\in H^1(k,C)$ map to the trivial class in $H^1(k,G)$. Its image
$$
i_ \ast(\alpha)\in H^1(k,P)
$$
also maps to the trivial class in $H^1(k,G)$, so $i_ \ast(\alpha)=1$. Applying $\rho_ \ast$ gives
$$
\alpha=(\rho\circ i)_ \ast(\alpha)=\rho_ \ast(i_ \ast(\alpha))=1.
$$

Thus $H^1(k,C)\to H^1(k,G)$ has trivial kernel. $\square$

Now return to $\lambda,\mu$. Assume that $\lambda_ K$ and $\mu_ K$ are $G(K)$-conjugate. Define the transporter
$$
X:=\operatorname{Transp}_ G(\lambda,\mu)=\\\{
g\in G:\operatorname{Int}(g)\circ\lambda=\mu
\\\}.
$$

This is a closed $k$-subscheme of $G$. Since $\lambda_ K$ and $\mu_ K$ are $G(K)$-conjugate, we have
$$
X(K)\neq\varnothing.
$$

Let
$$
C:=C_ G(\lambda).
$$

The group $C$ acts on $X$ on the right by multiplication. This action is simply transitive after any field extension over which $X$ has a point: if $x,y\in X$, then
$$
x^{-1}y\in C_ G(\lambda).
$$

Thus $X$ is a right $C$-torsor over $k$. Let
$$
[X]\in H^1(k,C)
$$
be its cohomology class.

Now induce this torsor from $C$ to $G$. The associated $G$-torsor is
$$
X\times^C G.
$$

But there is a natural $G$-equivariant isomorphism
$$
X\times^C G \xrightarrow{\sim} G,
\qquad
[x,a]\longmapsto xa.
$$

Therefore the image of $[X]$ in $H^1(k,G)$ is trivial. By the lemma,
$$
[X]=1\in H^1(k,C).
$$

Hence the $C$-torsor $X$ is trivial, so
$$
X(k)\neq\varnothing.
$$

Choose $h\in X(k)$. By definition of $X$,
$$
\operatorname{Int}(h)\circ\lambda=\mu.
$$

Thus $\lambda$ and $\mu$ are $G(k)$-conjugate.

Therefore the map
$$
\mathbb X_ \ast(G)/G(k)\longrightarrow \mathbb X_ \ast(G_ K)/G(K)
$$
is injective.
