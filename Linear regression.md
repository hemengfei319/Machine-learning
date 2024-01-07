# Linear regression

Training set-Data used to train the model.

Notation:

- x = "input" variable feature
- y = "output"variable、"target"variable
- m = number of training examples
- ( x , y ) = single training example
- $\left(x^{({i})},y^{({i})}\right)$ =  $i^{{th}}$ training example
- $\hat{y}$ = predictionn (estimated y)
- $f$(function) = mdel

$fw、b\left(x\right)=wx+b$

## Cost Function $J\left(w,b\right)$ 

Mdel:  $fw、b\left(x\right)=wx+b$

$w,b$ : parameters/coefficients/weights

$\hat{y}$ =$fw、b\left(x^{({i})}\right)$  = $wx^{({i})}+b$ 

$J\left(w,b\right) =  \frac{1}{2m}\underset{i=1}{\overset{m}{\sum}}\left(\hat{y}^{(i)}-y^{(i)}\right)^2$  ----- Squared error cost function

$J\left(w,b\right) =  \frac{1}{2m}\underset{i=1}{\overset{m}{\sum}}\left(fw、b\left(x^{({i})}\right)-y^{(i)}\right)^2$  

goal ; $\ _{w,b}^{minimize}J\left(w,b\right)$ 
