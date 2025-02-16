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

To prove that $O(log_2n)$ and $0(log_5n)$ are asymptotically the same, we need to prove that they are the same as $n\rightarrow\infin$. Using the change of base formula $\log_ba=\frac{\log_ca}{\log_cb}$, we can compare logarithms with different bases in terms of logarithms with a common base. In this case applying the formula we get $\frac{log_2n}{log_5n}=log_25$, but this can be done with logarithms with any base. 

By the Big-O noation, we say that $f(n) \in O(g(n))$ if $f(n) \le c \cdot g(n)$ for some postive value of $c$. By subsituting $f(n) = log_2n$ and $g(n) = log_5n$, we get $log_2n \le c \cdot log_5n$. As we found a a value of $c$ that makes this statment true, we can say $log_2n \in O(log_5n)$. By the same process we can also prove that $log_5n \in O(log_2n)$. From this we can conclude that $O(log_2n) = O(log_5n)$.

## Sources
Much credit goes to my youngest brother Jaxon Hepworth is the one who gave me the idea to use the change of base formula for logarithms.

I certify that I have listed all sources used to complete this exercise, including the use of any Large Language Models. All of the work is my own, except where stated otherwise. I am aware that plagiarism carries severe penalties and that if plagiarism is suspected, charges may be filed against me without prior notice.
