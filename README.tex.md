# Data-Science-Notes
Notes about Data Science, Machine Learning, Deep Learning &amp; Artificial Intelligence

## Deep Learning : Basics

### Perceptron

$x.\omega = x_1*\omega_1 + x_2*\omega_2 + \dots + x_n*\omega_n$

$z = x.\omega + b$

$\hat{y} = \sigma(z) = \frac{1}{1 + \exp(-z)}$


the higher the bias, the easier the neuron will activate

### Backpropagation (with a Perceptron)

example with a regression problem 

$$\boxed{C = MSE = \frac{1}{n}\sum_{i=1}^{n} (y_i - \hat{y_i})^2}$$

chain rule

$$\boxed{\frac{\partial C}{\partial \omega_i} = \frac{\partial C}{\partial \hat{y}} * \frac{\partial \hat{y}}{\partial z} * \frac{\partial z}{\partial \omega_i}}$$

$\frac{\partial C}{\partial \hat{y}} = \frac{2}{n}\sum_{i=1}^{n} (y_i - \hat{y_i}) = \frac{2}{n}sum(y - \hat{y})$

$\frac{\partial \hat{y}}{\partial z} = \frac{\partial}{\partial z}\sigma(z) = \frac{\exp(-z)}{(1 + exp(-z))^2} = \frac{1}{1 + exp(-z)} * \frac{\exp(-z)}{1 + exp(-z)}$

so :

$\frac{\partial \hat{y}}{\partial z} = \frac{1}{1 + exp(-z)} * (1 - \frac{1}{1 + exp(-z)}) = \sigma(z) * (1 - \sigma(z))$

$\frac{\partial z}{\partial \omega_i} = \frac{\partial}{\partial \omega_i}\sum_{i=1}^{n} (x_i * w_i + b) = x_i$

$\frac{\partial z}{\partial b} = \frac{\partial}{\partial b}\sum_{i=1}^{n} (x_i * w_i + b) = 1$

finally :

$$\boxed{\frac{\partial C}{\partial \omega_i} = \frac{2}{n} * sum(y - \hat{y}) * \sigma(z) * (1 - \sigma(z)) * x_i}$$
$$\boxed{\frac{\partial C}{\partial b} = \frac{2}{n} * sum(y - \hat{y}) * \sigma(z) * (1 - \sigma(z))}$$ 

### Optimization : Gradient Descent

Given the learning rate $\eta$ :

$$\boxed{\omega_i = \omega_i - \eta * \frac{\partial C}{\partial \omega_i}}$$
$$\boxed{b = b - \eta * \frac{\partial C}{\partial b}}$$

we update this way in order to decrease the cost
