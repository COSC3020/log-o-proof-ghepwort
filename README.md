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
To prove that $O(log_2n)$ is the same as $O(log_5n)$ we must prove that $log_2n$ and $log_5n$ are the same asymptoticly. In asymptotic analysis, constant factors do not change the big-O classification, so functions that differ only bas a constant multiple belong to the same big-O class. This means that at large values, if there is some constant $c$ where $log_5n=c \cdot log_2n$ then asymptoticaly $O(log_2n)$ is the same as $O(log_5n)$. The change of base formula for logarithms is: $log_ba=\frac{log_ca}{log_cb}$ or $log_cb=\frac{log_ca}{log_ba}$. By rearanging the previous equation we get $c=\frac{log_5n}{log_2n}=log_52$ which is a constant. As we have proven $log_5n$ and $log_2n$ differ by a constant factor, then asymptoticly $O(log_2n)$ and $O(log_5n)$ must be the same.


## Sources
Much credit goes to my youngest brother Jaxon Hepworth is the one who gave me the idea to use the change of base formula for logarithms.

I certify that I have listed all sources used to complete this exercise, including the use of any Large Language Models. All of the work is my own, except where stated otherwise. I am aware that plagiarism carries severe penalties and that if plagiarism is suspected, charges may be filed against me without prior notice.