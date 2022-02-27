<style>
  @counter-style chap6 {
    system: extends decimal;
    prefix: "6.";
  }
  ol {
    list-style: chap6;
  }
  ol ol {
    list-style: decimal
  }
</style>

# Burger Textbook - Chapter 6
## Lucas LaValva

1) 
    statement | evaluation
    :- | :-
    $\emptyset\in A$ | false, but $\emptyset\subseteq A$ 
    $A\subseteq A$ | true
    $A\cap B\subseteq A\cup B$ | true
    $(A\ \backslash\ B)\ \backslash\ C=A\ \backslash\ (B\ \backslash\ C)$ | false, but $(A\ \backslash\ B)\ \backslash\ C\subseteq A\ \backslash\ (B\ \backslash\ C)$
    $A\cup(B\cap C)=(A\cap B)\cup(A\cap C)$ | false, $A\cap(B\cup C)=(A\cap B)\cup(A\cap C)$
    $A\ \backslash\ B\subseteq A$ | true
    $A\subseteq B\iff A\cup B=B$ | true

2) This statement is false, but it would be true if the function was one-to-one.
3) Since $X$ and $Y$ are finite, we can be sure that $|f(X)|\leq |X|$ and $|f(X)|\leq Y$.
4) This must be true, because the definition of a function states that there exists a unique $z$ for each $y$, and a unique $y$ for each $x$. Thus, by the transitive property, there must be some unique $z$ for each $x$ such that $(g\circ f)(x)=z$.
5) 
    1-1 | onto | $f(x)$
    :-- | :--- | :--
    $\checkmark$ | $\checkmark$ | $x$
    $\checkmark$ | $\times$ | $e^x$
    $\times$ | $\checkmark$ | $x\sin (x)$
    $\times$ | $\times$ | $\sqrt{5 - x^2}$
6) 
    1) $f, g$ (one-to-one) $\implies g\circ f$ (one-to-one)
        
        Since $x$ and $g$ are both one-to-one, we know that
        $$
          f(x_1)=f(x_2)\implies x_1=x_2
        $$
        and
        $$
          g(y_1)=g(y_2)\implies y_1=y_2.
        $$
        Therefore,
        $$
          g\circ f(x_1)=g\circ f(x_2)\implies f(x_1)=f(x_2)\implies x_1=x_2
        $$
    2) $f, g$ onto $\implies g\circ f$ onto

        Since $f$ and $g$ are onto, we can be certain that
        $$
          f(X) = Y
        $$
        and
        $$
          g(Y) = Z.
        $$
        Thus,
        $$
          g\circ f(X)=g(Y)=Z
        $$
7) This statement is false. Consider the function $f:\mathbb{R\to R}$ such that $f(x)=x^2$. Then $f^{-1}(x)=\sqrt{x}$ which is not a function. The statement _is_ true for **one-to-one** functions.
8) This statement is false. Consider the function $f:\mathbb{Z\to 2Z}$ such that $f(x)=2x$. This is clearly a function, but $|\mathbb{Z}|\neq |2\mathbb{Z}|$. On the other hand, the statement would have been true for _finite_ functions.
9) $f(x)=2x$
10) This statement is false, but it is true for functions that are both one-to-one _and_ onto.
11) $$
      \{\} \\
      \{\spades\} \\
      \{\diamonds\} \\
      \{\hearts\} \\
      \{\clubs\} \\
      \{\spades,\diamonds\} \\
      \{\spades,\hearts\} \\
      \{\spades,\clubs\} \\
      \{\diamonds,\hearts\} \\
      \{\diamonds,\clubs\} \\
      \{\hearts,\clubs\} \\
      \{\spades,\diamonds,\hearts\} \\
      \{\spades,\diamonds,\clubs\} \\
      \{\spades,\hearts,\clubs\} \\
      \{\diamonds,\hearts,\clubs\} \\
      \{\spades,\diamonds,\hearts,\clubs\}
    $$
12) Let $a_k,k< n$ be the $k$th item in $A$ after it has been mapped to $\mathbb{Z}_n$. Then for any $p\in \mathcal{P}(A)$,
    ```py
    def f(p):
      return ''.join(('1' if i in p else '0') for i in range(n))
    ```
    This function is onto because there are 2 options for each index and therefore $2^n$ possible solutions, and $|\mathcal{P}(A)|=2^{|A|}=2^n$.
13) Since $f$ from problem 6.12 is one-to-one and onto, we know that $f^{-1}$ maps binary strings of length $n$ to $\mathcal{P}(A)$, given that $|A|=n$. Thus, to find all values of $\mathcal{P}(A)$ we can count to $2^n$ in binary and map each value to one in $\mathcal{P}(A)$.
14) _Skipped_
15) $$
      f(x)=\begin{cases}
        \frac{x}{2} & x =\left(\frac{1}{2}\right)^n, n\in \mathbb{N} \\
        x & x\neq \left(\frac{1}{2}\right)^n
      \end{cases}
    $$