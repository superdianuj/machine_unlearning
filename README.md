# machine_unlearning
Performing machine unlearning via gradient descent, instead of gradient ascent

This work basically was inspired by the original Machine unlearning paper, and I was surprised that basic graident ascent was not considered in that paper. Instead of wierd training data allocation scheme was devised.

But on the other hand, in later papers, machine unlearning via gradient ascent was considered. 

I hereby replace the ascent with descent by minimizing $\frac{1}{1+L(x,y)}$ instead of maximizing $L(x,y)$, where {x,y} is the data sample to be unlearned.
