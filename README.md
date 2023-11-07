# machine-learning-from-scratch
Machine Learning and Deep Learning Algorithms from Scratch


Log Loss of Logistic Regression

imagine you have a game where you try to guess whether a hidden object is a red ball (1) or a blue ball (0). You want to get really good at guessing. To do that, you need to practice and learn from your mistakes.

Now, think of a special score that tells you how good or bad your guesses are. We'll call this score "the Guessing Score."

If you guess "red ball" (1) when it's actually a red ball, your Guessing Score gets better.

If you guess "red ball" (1) when it's actually a blue ball, your Guessing Score gets worse.

If you guess "blue ball" (0) when it's actually a blue ball, your Guessing Score gets better.

If you guess "blue ball" (0) when it's actually a red ball, your Guessing Score gets worse.

Your goal is to get a high Guessing Score, which means you're making really good guesses.

In the game, you want to find the best way to guess, and you use a special formula to calculate your Guessing Score after each guess. This formula is like a magic recipe, and it looks like this:

Guessing Score = -[your guess (0 or 1) * log(probability of your guess) + (1 - your guess) * log(1 - probability of your guess)]

Here's what this means:

Your guess is either 0 (for "blue ball") or 1 (for "red ball").

The "probability of your guess" is like how sure you are that your guess is correct. If you're very sure, the probability is close to 1. If you're not sure at all, the probability is close to 0.

The formula helps you see how good or bad your guess is, based on how sure you were and whether your guess matched the real color.

So, in your game, you use this formula to calculate your Guessing Score after each guess. Your goal is to make your Guessing Score as high as possible by getting better and better at guessing the right color. This way, you become a pro at guessing red and blue balls


The loss function commonly used in logistic regression is the Cross-Entropy Loss, also known as Log Loss. It's a suitable choice for binary classification problems where the target variable has two possible outcomes, typically represented as 0 and 1. The logistic regression loss function is defined as follows:

For a single training example with the true label (target) denoted as y (0 or 1) and the predicted probability of the positive class (class 1) denoted as p(y=1), the logistic regression loss can be expressed as:

Log Loss (Cross-Entropy Loss):

scss
Copy code
L(y, p(y=1)) = -[y * log(p) + (1 - y) * log(1 - p)]
Here's what each part of this equation represents:

L(y, p(y=1)): This is the loss for a single training example.
y: The true label (0 or 1) for the training example.
p(y=1): The predicted probability that the instance belongs to class 1 (the positive class).
The loss function has two components:

The first term, -y * log(p), measures the loss when the true label is 1 (y=1). It quantifies how well the model's prediction aligns with the actual positive cases. If the model predicts a high probability for the positive class (p ≈ 1) when y=1, the loss is low.

The second term, -(1 - y) * log(1 - p), measures the loss when the true label is 0 (y=0). It quantifies how well the model's prediction aligns with the actual negative cases. If the model predicts a high probability for the negative class (p ≈ 0) when y=0, the loss is low.

The overall loss is a weighted combination of these two terms based on the true label y. The goal during training is to minimize this loss function, typically using optimization techniques like gradient descent. Minimizing the loss encourages the model to make accurate predictions for both positive and negative cases.

Logistic regression aims to find the model parameters (coefficients) that minimize the average log loss across all training examples, resulting in a model that can make accurate binary classifications.
