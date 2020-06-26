# Data-Science-Notes
Notes about Data Science, Machine Learning, Deep Learning &amp; Artificial Intelligence

## Deep Learning : Basics

### Perceptron

$x.\omega = x_1*\omega_1 + x_2*\omega_2 + \dots + x_n*\omega_n$

$z = x.\omega + b$

$\hat{y} = \sigma(z) = \frac{1}{1 + \exp(-z)}$

### Backpropagation (with a Perceptron)

example with a regression problem 

$$C = MSE = \frac{1}{n}\sum_{i=1}^{n} (y_i - \hat{y_i})^2$$

chain rule

$$\frac{\partial C}{\partial \omega_i} = \frac{\partial C}{\partial \hat{y}} * \frac{\partial \hat{y}}{\partial z} * \frac{\partial z}{\partial \omega_i}$$

$\frac{\partial C}{\partial \hat{y}} = \frac{2}{n}\sum_{i=1}^{n} (y_i - \hat{y_i})$

$\frac{\partial \hat{y}}{\partial z} = \frac{\partial}{\partial z}\sigma(z) = \frac{\exp(-z)}{(1 + exp(-z))^2} = \frac{1}{1 + exp(-z)} * \frac{\exp(-z)}{1 + exp(-z)} = \frac{1}{1 + exp(-z)} * (1 - \frac{1}{1 + exp(-z)})$

