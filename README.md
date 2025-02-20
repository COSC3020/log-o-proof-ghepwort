# Asymptotic Equivalences

In the lectures, we said that logarithms with different bases don't affect the
asymptotic complexity of an algorithm. Prove that $O(\log_{2} n)$ is the same as
$O(\log_{5} n)$. Use the mathematical definition of $O$ -- do a formal proof,
not just the intuition.

I have started with the formal definition of $O$ below. Add your answer to this
markdown file. [This
page](https://docs.github.com/en/get-started/writing-on-github/working-with-advanced-formatting/writing-mathematical-expressions)
might help with the notation for mathematical expressions.

$T(n) \in O(f(n)) \iff \exists c, n_0: T(n) \leq c \cdot f(n) \forall n \geq n_0$

## Answers

To show that $O(log_2n) = O(log_5n)$, we must prove that any function $f(n)$ that belongs to $O(log_2n)$ also belongs to $O(log_5n)$ and vise versa. The key tool is the logarithm change of base formula, which states $log_2n = log_25 \cdot log_5n$. and $log_5n = log_52 \cdot log_2n$ where $log_25$ and $log_52$ are both positive constants. 

Suppose $f(n) \in O(log_2n)$, meaning there exists a constant $c_0>0$ such that we have $f(n) \le c_0 \cdot log_2n$. Substituting $log_2n = log_25 \cdot log_5n$, we see obtain $f(n) \le c_0 \cdot log_25 \cdot log_5n$. Setting another constant $c_1 = c_0 \cdot log_25$, we see that $f(n) \le c_1 \cdot log_5n$, proving $f(n) \in O(log_5n)$.

Similary, if $f(n) \in O(log_5n)$, then there exists a constant $b_0 > 0$ such that $f(n) \le b_0 \cdot log_5n$. Substituting $log_5n = log_52 \cdot log_2n$, we obtain that $f(n) \le b_0 \cdot log_52 \cdot log_2n$. Setting another constant $b_1 = b_0 \cdot log_52$, we see that $f(n) \le b_1 \cdot log_2n$, proving $f(n) \in O(log_2n)$. 

Since we have proven that $O(log_2n)$ is in $O(log_5n)$ and that $O(log_5n)$ is in $O(log_2n)$, it follows that $O(log_2n) = O(log_5n)$ proving that they are asymptotically equivalent.


## Sources
Much credit goes to my youngest brother Jaxon Hepworth is the one who gave me the idea to use the change of base formula for logarithms.

Noah Vougt Helped me realize that to prove the biconditional I had to prove both was so I didn't assume a specific f(n).

I certify that I have listed all sources used to complete this exercise, including the use of any Large Language Models. All of the work is my own, except where stated otherwise. I am aware that plagiarism carries severe penalties and that if plagiarism is suspected, charges may be filed against me without prior notice.
