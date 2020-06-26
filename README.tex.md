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

$\frac{\partial C}{\partial \hat{y}} = \frac{2}{n}\sum_{i=1}^{n} (y_i - \hat{y_i}) = \frac{2}{n}sum(y - \hat{y})$

$\frac{\partial \hat{y}}{\partial z} = \frac{\partial}{\partial z}\sigma(z) = \frac{\exp(-z)}{(1 + exp(-z))^2} = \frac{1}{1 + exp(-z)} * \frac{\exp(-z)}{1 + exp(-z)}$

so :

$\frac{\partial \hat{y}}{\partial z} = \frac{1}{1 + exp(-z)} * (1 - \frac{1}{1 + exp(-z)}) = \sigma(z) * (1 - \sigma(z))$

$\frac{\partial z}{\partial \omega_i} = \frac{\partial}{\partial \omega_i}\sum_{i=1}^{n} (x_i * w_i + b) = x_i$

finally :

$$\frac{\partial C}{\partial \omega_i} = \frac{2}{n} * sum(y - \hat{y}) * \sigma(z) * (1 - \sigma(z)) * x_i$$
$$\frac{\partial C}{\partial b} = \frac{2}{n} * sum(y - \hat{y}) * \sigma(z) * (1 - \sigma(z))$$ (the last derivative equals to 1 for the bias)


