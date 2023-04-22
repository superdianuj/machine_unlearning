# machine_unlearning
Performing machine unlearning via gradient descent, instead of gradient ascent

This work basically was inspired by the original Machine unlearning paper, and I was surprised that basic graident ascent was not considered in that paper. Instead of wierd training data allocation scheme was devised, which can have high storage and computation overhead, as compared to simple gradient ascent. This is evident from the first paper, where the number of unlearning samples leads to exponential computation overhead, which wouldnot be the case for gradient ascent.
![image](https://user-images.githubusercontent.com/47445756/233808862-8f8ac98e-6534-4c17-a89b-8a57fd52b368.png)


But on the other hand, in later papers, machine unlearning via gradient ascent was considered. 

I hereby replace the ascent with descent by minimizing $\frac{1}{1+L(x,y)}$ instead of maximizing $L(x,y)$, where {x,y} is the data sample to be unlearned, and $L(x,y)$ is the corresponding loss function.

Following is the comparison of relationship between $x$ and $1/(1+x)$ to understand, how the gradient descent would work.

![image](https://user-images.githubusercontent.com/47445756/233808532-f341ebc2-cd8f-4817-a3c9-cc453e174e2f.png)

For the case of MNIST classification model, it can be seen that in remembering particular sample, we use gradient descent, which minimizes the inverted loss, while the original intended loss increases, indicating that the model is unlearning a particular sample.

![image](https://user-images.githubusercontent.com/47445756/233808595-3c89b08c-9321-4ae6-ad7c-9c8514f1740b.png)

Following is the comparison of output probability vector, before and after unlearning a particular MNIST sample.
![image](https://user-images.githubusercontent.com/47445756/233808789-991994f7-9f88-498e-b8ac-748b2cfef86a.png)



