# Data-Science-Notes
Notes about Data Science, Machine Learning, Deep Learning &amp; Artificial Intelligence

## Deep Learning : Basics

### Perceptron

<img src="/tex/cd1af465673070924712e29f44de258a.svg?invert_in_darkmode&sanitize=true" align=middle width=278.18037224999995pt height=19.1781018pt/>

<img src="/tex/dcefb399da445788575064c2a9e0122d.svg?invert_in_darkmode&sanitize=true" align=middle width=82.2143553pt height=22.831056599999986pt/>

<img src="/tex/5d7a33a5d7c8478a30a4137dcd4725b7.svg?invert_in_darkmode&sanitize=true" align=middle width=149.54884065pt height=27.77565449999998pt/>

### Backpropagation (with a Perceptron)

example with a regression problem 

<p align="center"><img src="/tex/568c3c7ef269fcd55b503d6cbd9b4ca1.svg?invert_in_darkmode&sanitize=true" align=middle width=217.39876454999995pt height=59.3631192pt/></p>

chain rule

<p align="center"><img src="/tex/68b23df92af2a0aa8a642ae5a7904994.svg?invert_in_darkmode&sanitize=true" align=middle width=171.4716498pt height=48.186512549999996pt/></p>

<img src="/tex/9a13359788821e367c4a777fb8a3acf4.svg?invert_in_darkmode&sanitize=true" align=middle width=271.7854854pt height=28.92634470000001pt/>

<img src="/tex/a7d203411fd149b4d767d7184e2f1bc1.svg?invert_in_darkmode&sanitize=true" align=middle width=367.407678pt height=33.20539859999999pt/>

so :

<img src="/tex/a2f9473a2840ced0f17683f5447e204b.svg?invert_in_darkmode&sanitize=true" align=middle width=372.84301065pt height=30.648287999999997pt/>

<img src="/tex/5e6ee175f78b83a39ac923f1c4a8c3d9.svg?invert_in_darkmode&sanitize=true" align=middle width=236.00524860000002pt height=28.92634470000001pt/>

<img src="/tex/98324c53b34b9b637cc14608d5965a3c.svg?invert_in_darkmode&sanitize=true" align=middle width=215.73438314999999pt height=28.92634470000001pt/>

finally :

<p align="center"><img src="/tex/b0e3e6eef25b55bd1a0b91cf4ca77947.svg?invert_in_darkmode&sanitize=true" align=middle width=342.84876119999996pt height=47.45589585pt/></p>
<p align="center"><img src="/tex/5153ca566c3930e7ab22306f72854127.svg?invert_in_darkmode&sanitize=true" align=middle width=305.0843631pt height=44.990167199999995pt/></p> 

### Optimization : Gradient Descent

Given the learning rate <img src="/tex/1d0496971a2775f4887d1df25cea4f7e.svg?invert_in_darkmode&sanitize=true" align=middle width=8.751954749999989pt height=14.15524440000002pt/> :

<p align="center"><img src="/tex/b8805f112b549d100d5bc2e77b9c1ea8.svg?invert_in_darkmode&sanitize=true" align=middle width=138.16406174999997pt height=47.45589585pt/></p>
<p align="center"><img src="/tex/34c1fbd1c7597990bc115830e2da1d1b.svg?invert_in_darkmode&sanitize=true" align=middle width=118.08353865pt height=44.990167199999995pt/></p>

we update this way in order to decrease the cost
