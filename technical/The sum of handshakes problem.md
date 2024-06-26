# The sum of Handshakes Problem

When I was young, a friend gave me a puzzle, `how many handshakes are there in a meeting of 10 persons where everyone must shake hands once and only once?`. That time I had no means that I could find the answer fast. [pause a minute to try to find the answer].

## Arithmetic Progression Approach
The only efficient way for the persons to shake hands is to line them in order something like a line.

[[image]]

The last(10th) person must start shaking all other persons' hands which will be $9$ handshakes. Then the `9th` person must shake all other participants, she doesn't have to shake the `10th` person because that handshake is already counted for, in the first count. This `9th` person will have to make 8 handshakes.

As you may notice the pattern continues, every preceding does not have to shake hands with those that have already shaken hands with everyone. Then the number of handshakes will be $9,8,7,6,5,4,3,2,1$ and it has to be clear that the first person does not have to shake anyone's hands and can't shake his own hand then the sum of all handshakes is $1+2+3+4+5+6+7+8+9$

That time I was presented with this problem I had to add these up. I did not know anything about Arithmetic Progression. This is the sum of the first `n-terms` which can be easily found by $\frac{n(n + 1)}{2}$ in our case which is $\frac{9(9 + 1)}{2} = 45$.

Now that we have found out what we were looking for, what about the sum of handshakes of M persons? It is clear from the previous 10-persons that we had $10 - 1$ to find the sum of $n = 9$ first numbers. Then for M persons we have to get the sum of `M-1` terms which is $\frac{n(n + 1)}{2} = \frac{(M-1)((M-1) + 1)}{2} = \frac{M(M-1)}{2}$

## Combinatorial Approach
But this is not interesting enough. We can still go back to our original problem `How many handshakes are there in a meeting of 10 persons where everyone must shake everyone once and only once`. We can look at this from a different perspective, the 10-person in a meeting can be taken as a set which makes this a 10-membered set and every handshake happens between two persons and exactly two persons. Then we can find the number of handshakes that are there in a 10-person meeting by counting the number of 2-person subsets that are there in a 10-membered set. And from combinatorics, we know that this is $\binom{n}{r}$, where `n = 2` and `r = 2` making the total $\binom{10}{2} = 45$, which is exactly what we found with the AP formula. We can then find the sum of any M-persons handshakes by $\binom{M}{2}$

The interesting result is that $\binom{M}{2} = \frac{M(M-1)}{2}$

There exist other proofs that find the same result but I found this interesting enough because it is found while solving a seemingly simple problem.

## Related Links
These links provide further reading into the subject matter and some other approaches to our concluded identity.

It might be worth saying that I found the identity somehow independently while reading `Discrete Mathematics: Elementary and Beyond` - László Lovász, Jozsef Pelikan, Katalin L. Vesztergombi. With a simple search on the internet, it seems that the proof of it using the sum of handshakes was also already discovered.

- [what is n choose 2?](https://www.storyofmathematics.com/n-choose-2/)
- [Binomial Coefficients](https://nrich.maths.org/7713)
- [N Choose 2 is the Sum of the First N-1 Integers](https://www.jeremykun.com/2011/10/02/n-choose-2/)
- [Combinations- Involving Several Sets](https://math.libretexts.org/Bookshelves/Applied_Mathematics/Applied_Finite_Mathematics_(Sekhon_and_Bloom)/07%3A_Sets_and_Counting/7.06%3A_Combinations-_Involving_Several_Sets)
