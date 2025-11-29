This game comes from a traditional finger game.

Let there be two player Alice and Bob. Each player has an array of length $2$. At the start of the game, each player got an array $[1, 1]$.

Let $A$ be Alice's array and $B$ be Bob's array.

Let $M_L$ be the first element and $M_R$ be the second element of an array $M$. So for example, $A_L$ is Alice's first element; $B_R$ is Bob's second element.

This game is a turn-based game, and Alice starts first.

At each turn, let $M$ be the current player's array and $E$ be the opponent's array. The player can do **one** of the following.

- **Defense move**: pick some nonzero integer $r$ and let $M' = [M_L + r, M_R - r]$ such that $M'$ is **not** a permutation of $M$ and $0 \leq M'_L, M'_R < K$. And then set $M := M'$.
- **Offensive move**: pick some nonzero element of $M$—let's say $m$—and add $m$ to one of nonzero element of $E$. After that set $E_L := E_L \bmod K$ and $E_R := E_R \bmod K$.

If at any point an element becomes zero, then that element is called “dead”. For example, if $A_L = 0$, then Alice's first element is dead. A dead element can be “revived” using the defensive move. For example, let $M = [3, 0]$ and $r = -2$, therefore $M' = [1, 2]$, reviving $M_R$.

The first one to have all elements dead, will lose and the game ends. Or in formal words, the first one to have an array $[0, 0]$ will lose.

The usual game has $K$ set to $5$.

---

What if $K$ is not $5$ anymore …? Let's say, $K = 4$. Or maybe $K = 1000$.