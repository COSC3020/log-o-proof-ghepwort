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

To prove that $O(log_2n)$ and $O(log_5n)$ are asymptotically the same, we need to prove that they are the same as $n\rightarrow\infin$. Using the change of base formula $\log_ba=\frac{\log_ca}{\log_cb}$, we can compare logarithms with different bases in terms of logarithms with a common base. In this case applying the formula we get $\frac{log_2n}{log_5n}=log_25$. Solving out we get $log_2n=log_25 \cdot log_5n$.

By the Big-O noation, we say that $f(n) \in O(g(n))$ if $f(n) \le c \cdot g(n)$ for some postive value of $c$. By subsituting $f(n) = log_2n$ and $g(n) = log_5n$, we get $log_2n \le c \cdot log_5n$. As we found a value of $c$ that makes this statment true, we can say $log_2n \in O(log_5n)$. However, we can't assume a particular $f(n)$. Re-solving the earlier equation we get that $log_5n = \cdot \frac{1}{log_52}log_2n$. By substituting $f(n) = log_5n$ and $g(n) = log_2n$, we get that $log_5n \le c \cdot log_5n$. As we have found a value of $c$ that makes this statment true, we can say $log_5n \in O(log_2n)$.

As we have proven $log_2n \in O(log_5n)$ and $log_5n \in O(log_2n)$, then we can conclude that $O(log_2n)$ and $O(log_5n)$ are asymptotically the same.

## Sources
Much credit goes to my youngest brother Jaxon Hepworth is the one who gave me the idea to use the change of base formula for logarithms.

Noah Vougt Helped me realize that to prove the biconditional I had to prove both was so I didn't assume a specific f(n).

I certify that I have listed all sources used to complete this exercise, including the use of any Large Language Models. All of the work is my own, except where stated otherwise. I am aware that plagiarism carries severe penalties and that if plagiarism is suspected, charges may be filed against me without prior notice.
