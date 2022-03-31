# Cows, Bulls and Beyond: Optimal solutions for common code-breaking games

[lukelavalva.com/informationtheory](http://lukelavalva.com/informationtheory)

Check it out, I've made some progress.

## Introduction
- Explanation of _Cows and Bulls_
- Transition into _Mastermind_
- Interactive Mastermind Game

## Framing _Mastermind_ in terms of information theory
- Introduction of the Solution Space
  - All solutions for the Mastermind game can be represented in an $n$-dimensional grid
- Interactive solution space for a much smaller version of _Mastermind_
  - 2 digits and 4 colors = 16 possible solutions
  - Interactive version allows the person to adjust the number of digits and colors, but default is (2, 4).
- Explanation of exactly _how_ the solution space is reduced by each answer
  - The distance between each set of two words may be represented as a length 3 vector $\langle$Red Pegs, White Pegs, Empty Peg Slots$\rangle$, where the three digits of the vector add up to the length of the words.
  - After the response has been given for a word, we may eliminate all words that have a greater($^*$) distance than the reponse given.
    - Let $g$ represent the word that was presented as a guess and $r$ be the response that was provided for the guess, while $d(w_1, w_2)$ represents the distance vector between words $w_1$ and $w_2$. Then a word $w$ may be eliminated if
      $$
        \max(d(g, w) - r) > 0.
      $$

## Heuristic Strategies for _Mastermind_
- Donald Knuth's implementation of the **minimax** algorithm, AKA "Worst Case" heuristic
  - Intuitive strategy after the game is viewed as one in which the solution space is minimized each move
  - For each turn, each possible guess should be evaluated to find out how much it could reduce the solution space.
  - Since we don't know what the response is going to be for each code, we must figure out a metric to use for determining which reduces the space most
    - Knuth's decision was to **maximise** the worst case (response that reduces the space **minimally**), hence his use of the minimax algorithm.
  - This is guaranteed to solve a standard _Mastermind_ game in $\leq 5$ moves no matter what, with an average of 4.476 moves
    - It may be adjusted slightly for an average of 4.467 using index manipulation (Gur 2021)
- Expected Size
  - Sum the squares of the number of guesses left after each response has been given.
  - Essentially finding expected value of each response.
  - For a given guess $g$, find the expected value with
    $$
      E(g) = \sum_r P(g, r)^2
    $$
- Weighted Average Entropy Across Guesses
  - For any guess $g$ and response $r$, let $P(g, r)$ represent the reduction of the solution space as a proportion. Then the entropy of a given guess and response is calculated by
    $$
      I(g, r)=-\log_2(P(g, r))
    $$
  - We can find the expected value for the entropy of any guess with
    $$
      E(g) = \sum_r P(g, r)I(g, r)
    $$
  - For each guess, we may choose the code that has the highest expected entropy
  - This is guaranteed to solve $M_{4, 6}$ in 6 or fewer moves, with an average of 4.357 moves.
- Interactive componenet where these metrics may be explored

## Optimal Strategy for _Mastermind_
- Using a depth first search, it is possible to analyze ALL possible solutions for _Mastermind_
- This is not practical, and before a computer found all solutions the sun would explode
- Using pruning and various other search techniques, it is possible to find the set of provably optimal solutions for $M_{4, 6}$.
- This still takes a pretty long time