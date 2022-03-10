<style>
  @counter-style chap6 {
    system: extends decimal;
    prefix: "7.";
  }
  ol {
    list-style: chap6;
  }
  ol ol {
    list-style: decimal
  }
</style>

# Burger Textbook - Chapter 7
## Lucas LaValva

1. Suppose $\mathbb{N}$ is not an infinite set. Then there must exist some $n$ so that $|S|=|\{1, 2, \ldots, n\}|$. However, for any $n$ it is clear that $\{1, 2, \ldots, n\}\subset\mathbb{N}$. Thus, $\mathbb{N}$ is an infinite set.
2. This is true, consider the map $\phi:\mathbb{N}\to\{0\}\cup\mathbb{N}$ such that $\phi(n)=n-1$.
3. This is true, consider the map $\phi:\mathbb{N}\to\mathbb{Z}$ such that $\phi(n)=\lfloor n/2\rfloor(-1)^n$.
4. This is true, consider the following map $\phi$ from $\mathbb{N}$ to $\mathbb{Q}$:
    | $n$ | $\phi(n)$ | $n$ | $\phi(n)$ | $n$ | $\phi(n)$ | $n$ | $\phi(n)$ |
    | :-: | :-------- | :-: | :-------- | :-: | :-------- | :-: | :-------- |
    |  1  | $1/1$     | 11  | $4/1$     | 21  | $5/6$     | 31  | $7/5$     |
    |  2  | $1/2$     | 12  | $1/5$     | 22  | $6/5$     | 32  | $7/4$     |
    |  3  | $2/1$     | 13  | $2/5$     | 23  | $6/1$     | 33  | $7/3$     |
    |  4  | $1/3$     | 14  | $3/5$     | 24  | $1/7$     | 34  | $7/2$     |
    |  5  | $2/3$     | 15  | $4/5$     | 25  | $2/7$     | 35  | $7/1$     |
    |  6  | $3/2$     | 16  | $5/4$     | 26  | $3/7$     | 36  | $1/8$     |
    |  7  | $3/1$     | 17  | $5/3$     | 27  | $4/7$     | 37  | $3/8$     |
    |  8  | $1/4$     | 18  | $5/2$     | 28  | $5/7$     | 38  | $5/8$     |
    |  9  | $3/4$     | 19  | $5/1$     | 29  | $6/7$     | 39  | $7/8$     |
    | 10  | $4/3$     | 20  | $1/6$     | 30  | $7/6$     | ... | $\ldots$  |

    Note that each fraction includes two integers that are relatively prime with one another.
5. This statement is true. If $S_1$ and $S_2$ are countable, then there exists invertable functions $\phi_1:S_1\to\mathbb{N}$ and $\phi_2:S_2\to\mathbb{N}$. Then we can define some function $f:S_1\times S_2\to \mathbb{N\times N}$ so that for any $s_1\in S_1$ and $s_2\in S_2$, $f((s_1, s_2))=(\phi_1(s_1), \phi_2(s_2))$. We know that $\mathbb{N\times N}$ is countable, so $f^{-1}(\mathbb{N\times N})= S_1\times S_2$ must also be coutable.
6. We know that $|\{1, 2, \ldots, N\}|=N$, and that $|\mathcal{B}_N|=2^N$. However, for all $N\in \mathbb{N}$, $2^N>N$. Thus, the sets do not have the same cardinality and $|\mathcal{B}_N|$ is larger.
7. Suppose that there exists some mapping from $\mathbb{N}$ to $\mathcal{B}_\infty$. Then, after the mapping is found we could select digits along a diagonal as follows:
    | $n$ | $\phi(n)$ |
    | :-: | :-------- |
    |  1  | ***1***0100101... |
    |  2  | 1***1***010001... |
    |  3  | 01***0***10101... |
    |  4  | 110***1***0100... |
    |  5  | 1001***0***111... |
    |  6  | 10111***0***00... |
    |  7  | 001000***1***1... |
    |  8  | 1011011***0***... |

    and then generate a new string in $\mathcal{B}_\infty$ that contains the opposite of each digit that it found within $\phi(\mathbb{N})$. This clearly is not an element of $\phi(\mathbb{N})$, so it is a contradiction. Thus, $\mathcal{B}$ is not a countable set.
8. $\mathbb{R}$ is not a countable set. We can consider the same diagonal argument that was proposed in (7.7), where each digit in the newly generated number is a 6 if the digit in its corresponding value is 4, and 4 otherwise. The newly generated element will not be an element of $\phi(\mathbb{N})$.
9. If $S$ can be any set, then this statement is false because $\mathcal{P}(\{\})=\{\}$. However, the statement is true for non-empty sets because for any nonempty set $S_n$, $|\mathcal{P}(S_n)|=|\mathcal{B}_{|S_n|}|>|S_n|$.
10. Yes, $|\mathbb{R}|<|\mathcal{P}(\mathbb{R})|<|\mathcal{P}(\mathcal{P}(\mathbb{R}))|$.
11. Suppose that there exists some "mother of all infinities" which we will call $\aleph$. Then $|\aleph|<|\mathcal{P}(\aleph)|$. Clearly, this is a contradiction.
12. Common sources of set theory label "countable infinity" as $\aleph_0$ and the cardinality of the real numbers as $\aleph_1$. As far as I could find, there is little to no literature on decimal values for $\aleph$.  I do not fully understand why it is impossible to have an infinite set between $\aleph_0$ and $\aleph_1$, and this question requires further research and understanding. 
13. Transcendental numbers exist, and we know some of them. The most useful transcendental numbers are $\pi$ and $e$.
14. $S$ is the set of all numbers which may be explained using 50 lowercase english letters and spaces. Then, assuming that this function is well-defined (each set of characters always maps to the same number) the maximum possible size of $S$ is $27^{50}$. Thus, $S$ has to be a finite set. However, suppose that we analyze the element in the set described as  "`the smallest number not contained in the set`". This statement is absurd, but it is definitely contained in $S$. Thus, either $S$ is invalid or it regards that statement as gibberish and doesn't map it to an element.
15. Bertrand Russell's paradox states that there cannot be a set $S$ which contains all sets that don't contain themselves. The critical flaw with this set is that self-reference causes an infinite loop. A catch-all solution for preventing similar paradoxes is to disregard $S$ and its paradoxical counterparts as absurd and claim that they are not formal sets. 