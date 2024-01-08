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

$f_w,_b\left(x\right)=wx+b$

## Cost Function $J\left(w,b\right)$ 

Mdel:  $f_w,_b\left(x\right)=wx+b$

$w,b$ : parameters/coefficients/weights

$\hat{y} =f_w,_b\left(x^{({i})}\right)  = wx^{({i})}+b$ 

$J\left(w,b\right) =  \frac{1}{2m}\underset{i=1}{\overset{m}{\sum}}\left(\hat{y}^{(i)}-y^{(i)}\right)^2$  ----- Squared error cost function

$J\left(w,b\right) =  \frac{1}{2m}\underset{i=1}{\overset{m}{\sum}}\left(f_w,_b\left(x^{({i})}\right)-y^{(i)}\right)^2$  

goal ; $\ _{w,b}^{minimize}J\left(w,b\right)$ 

## Gradient Descent

Strat with some $w,b$ (set $ w =0,b=0$)

Keep changing $w,b$ to reduce $J\left(w,b\right)$ 

Until we settke at or near a minimum 

$w = w -\alpha\frac{\delta}{\delta w}J\left(w,b\right)$

$b = b -\alpha\frac{\delta}{\delta b}J\left(w,b\right)$ 

- $\alpha$ : Learing rate (0-1)

Simultaneous update

$tmp\_w = w -\alpha\frac{\delta}{\delta w}J\left(w,b\right)$

$tmp\_b = b -\alpha\frac{\delta}{\delta b}J\left(w,b\right)$

 ![截图](../Linear%20regression/18aa8047abc42fc5db189f1525e9b637.png)

## Learing Rate

 If $\alpha$ is too small Gradient descent may be slow.

if $\alpha$ is too large Gradient descent may: 

- Overshoot,never reach minimum
- Fail to converage,diverge

![截图](../Linear%20regression/2a0194a93e3d4199ff6be298ea058c19.png)

## Gradient Descent for Linear Regression

Linear regression model : $f_w,_b\left(x\right) = wx+b$ 

Cost function : $J\left(w,b\right) =  \frac{1}{2m}\underset{i=1}{\overset{m}{\sum}}\left(f_w,_b\left(x^{({i})}\right)-y^{(i)}\right)^2$ 

Gradient descent algrithm:

	repeat until convergence 

		$w = w -\alpha\frac{\delta}{\delta w}J\left(w,b\right)= w -\alpha\frac{1}{m}\underset{i=1}{\overset{m}{\sum}}\left(f_w,_b\left(x^{({i})}\right)-y^{(i)}\right)    x^{(i)}$

		$b = b -\alpha\frac{\delta}{\delta b}J\left(w,b\right) =  b -\alpha\frac{1}{m}\underset{i=1}{\overset{m}{\sum}}\left(f_w,_b\left(x^{({i})}\right)-y^{(i)}\right)$ 

- $\frac{\delta}{\delta w}J\left(w,b\right) =  \frac{1}{m}\underset{i=1}{\overset{m}{\sum}}\left(f_w,_b\left(x^{({i})}\right)-y^{(i)}\right)	x^{(i)}$
  - $\frac{\delta}{\delta w}J\left(w,b\right) =  \frac{\delta}{\delta w}\frac{1}{2m}\underset{i=1}{\overset{m}{\sum}}\left(f_w,_b\left(x^{({i})}\right)-y^{(i)}\right)^2=\frac{\delta}{\delta w}\frac{1}{2m}\underset{i=1}{\overset{m}{\sum}}\left(wx^{(i)}+b-y^{(i)}\right)^2=\frac{1}{m}\underset{i=1}{\overset{m}{\sum}}\left(f_w,_b\left(x^{({i})}\right)-y^{(i)}\right)    x^{(i)}$ 

- $\frac{\delta}{\delta b}J\left(w,b\right) =  \frac{1}{m}\underset{i=1}{\overset{m}{\sum}}\left(f_w,_b\left(x^{({i})}\right)-y^{(i)}\right)  $  
  - $\frac{\delta}{\delta b}J\left(w,b\right) =  \frac{\delta}{\delta b}\frac{1}{2m}\underset{i=1}{\overset{m}{\sum}}\left(f_w,_b\left(x^{({i})}\right)-y^{(i)}\right)^2=\frac{\delta}{\delta b}\frac{1}{2m}\underset{i=1}{\overset{m}{\sum}}\left(wx^{(i)}+b-y^{(i)}\right)^2=\frac{1}{m}\underset{i=1}{\overset{m}{\sum}}\left(f_w,_b\left(x^{({i})}\right)-y^{(i)}\right)    $

"Batch" gradient descent  :Each step of gradient descent uses all the training examples.
