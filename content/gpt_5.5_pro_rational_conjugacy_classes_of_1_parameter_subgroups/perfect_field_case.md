+++
title = "Perfect Field Case (gpt-5.5-pro-web)"
date = 2026-05-17
weight = 8
[extra]
math = true
+++

## Statement

Let $G$ be a (not necessarily reductive) smooth connected affine group over a perfect field $k$. Let $K$ be an algebraic field extension of $k$. Let
$$
\mathbb{X}_ \ast(G) := \mathrm{Hom}_ {k\text{-groups}}(\mathbb{G}_ m, G)
$$
be the set of $k$-homomorphisms. Let $G_ K$ be the base change of $G$ to $K$. Prove that
$$
\mathbb{X}_ \ast(G)/G(k) \to \mathbb{X}_ \ast(G_ K)/G(K)
$$
is injective. You can take for granted that this statement is true if $G$ is connected reductive over a field $k$.

## Proof

Let
$$
U:=R_ u(G)
$$
be the unipotent radical of $G$. Since $k$ is perfect and $G$ is smooth connected affine, $U$ is a smooth connected unipotent normal $k$-subgroup, and
$$
H:=G/U
$$
is a connected reductive $k$-group. Let
$$
q:G\to H
$$
be the quotient map.

We will prove that the natural map
$$
q_ \ast:\mathbb X_ \ast(G)/G(k)\longrightarrow \mathbb X_ \ast(H)/H(k)
$$
is injective. Then the result follows from the reductive case applied to $H$.

First recall two standard facts about smooth connected unipotent groups over perfect fields.

1. If $U$ is smooth connected unipotent over $k$, then $U$ is $k$-split. Hence
   $$
   H^1(k,U)=1.
   $$
   Indeed, $U$ has a normal $k$-composition series with quotients $\mathbb G_ a$, and $H^1(k,\mathbb G_ a)=0$.

2. If $T=\mathbb G_ m$ acts $k$-rationally on such a $U$, then every algebraic $1$-cocycle
   $$
   c:T\to U
   $$
   is a coboundary. Equivalently, any two $k$-sections of
   $$
   U\rtimes T\to T
   $$
   are conjugate by an element of $U(k)$.

Here is the proof of the second fact. Because $U$ is split and $T$ is split, there is a $T$-stable normal series
$$
1=U_ 0\subset U_ 1\subset\cdots\subset U_ n=U
$$
with $U_ i/U_ {i-1}\cong \mathbb G_ a$. So it suffices by induction to treat $U=\mathbb G_ a$. Then the $T$-action is given by a character $t\mapsto t^m$, and a cocycle is a regular function $f:\mathbb G_ m\to\mathbb G_ a$, hence a Laurent polynomial $f(t)\in k[t,t^{-1}]$, satisfying
$$
f(tt')=f(t)+t^m f(t').
$$

If $m=0$, this forces $f=0$. If $m\neq 0$, comparing Laurent monomials gives
$$
f(t)=a(1-t^m)
$$
for some $a\in k$. In either case
$$
f(t)=a-t\cdot a,
$$
so $f$ is a coboundary. The induction then proves the claim for $U$.

Now we prove that $q_ \ast$ is injective. Let
$$
\lambda,\mu\in \mathbb X_ \ast(G)
$$
and suppose that $q\circ\lambda$ and $q\circ\mu$ are $H(k)$-conjugate. Thus there is $\bar g\in H(k)$ such that
$$
q\circ\mu=\operatorname{Int}(\bar g)\circ q\circ\lambda.
$$

Since $H^1(k,U)=1$, the map
$$
G(k)\to H(k)
$$
is surjective. Choose $g\in G(k)$ lifting $\bar g$. Replacing $\lambda$ by $\operatorname{Int}(g)\circ\lambda$, we may assume
$$
q\circ\lambda=q\circ\mu.
$$

Set
$$
\nu:=q\circ\lambda=q\circ\mu:\mathbb G_ m\to H.
$$

Form the pullback group
$$
E:=G\times_ {H,\nu}\mathbb G_ m.
$$
Thus, for a $k$-algebra $R$,
$$
E(R)=\\{(x,t)\in G(R)\times R^\times : q(x)=\nu(t)\\}.
$$

There is an exact sequence
$$
1\to U\to E\to \mathbb G_ m\to 1.
$$

The cocharacters $\lambda$ and $\mu$ give two $k$-sections of $E\to\mathbb G_ m$:
$$
t\mapsto (\lambda(t),t),\qquad t\mapsto (\mu(t),t).
$$

Using the first section, we identify
$$
E\cong U\rtimes \mathbb G_ m,
$$
where $\mathbb G_ m$ acts on $U$ by conjugation through $\lambda$:
$$
t\cdot u=\lambda(t)u\lambda(t)^{-1}.
$$

Under this identification, the second section is given by a cocycle
$$
c(t)=\mu(t)\lambda(t)^{-1}\in U.
$$

By the unipotent cocycle fact above, there is $u\in U(k)$ such that
$$
c(t)=u\lambda(t)u^{-1}\lambda(t)^{-1}.
$$

Therefore
$$
\mu(t)=c(t)\lambda(t)=u\lambda(t)u^{-1}
$$
for every $t$. Hence
$$
\mu=\operatorname{Int}(u)\circ\lambda.
$$

Thus $\lambda$ and $\mu$ are $G(k)$-conjugate. So
$$
q_ \ast:\mathbb X_ \ast(G)/G(k)\to \mathbb X_ \ast(H)/H(k)
$$
is injective.

Now suppose $\lambda,\mu\in \mathbb X_ \ast(G)$ become $G(K)$-conjugate after base change to $K$. Applying $q_ K:G_ K\to H_ K$, the cocharacters
$$
(q\circ\lambda)_ K,\qquad (q\circ\mu)_ K
$$
are $H(K)$-conjugate. Since $H$ is connected reductive, the reductive case gives that
$$
q\circ\lambda
$$
and
$$
q\circ\mu
$$
are already $H(k)$-conjugate. By the injectivity of $q_ \ast$, $\lambda$ and $\mu$ are $G(k)$-conjugate.

Therefore
$$
\mathbb X_ \ast(G)/G(k)\longrightarrow \mathbb X_ \ast(G_ K)/G(K)
$$
is injective.
