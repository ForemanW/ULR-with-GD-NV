# ULR-with-GD-NV
Univariate linear regression with gradient descent and non-vectorized code.

This jupyter notebook takes a set of inputs (x = features[], y = targets[])
and optimizes a cost function J of a univariate linear regression model y=wx+b,
where m is the number of datapoints and J(w,b) = 1/2m * sum from i=1 to i=m of (f(x(i))-y(i)^2), using the algorithm:

repeat until convergence{<br />

w = w-alpha(d/dw)J(w,b)<br />

b = b-alpha(d/db)J(w,b)<br />

note:simultaneously update w and b<br />

}<br />

It seems to work pretty well, I had to normalize the features matrix because I had
trouble converging when the features were a wide range of values (thanks chatGPT, I
would not have thought of that). With a small range of x values, the features matrix
does not need to be normalized. 

Outputs to this code are the optimized values of w and b, a plot of the cost function
over iterations, and a plot of the data with the linear regression model of optimized
w and b drawn. 

I'd like to add an output of the cost function visualized in 3 dimensions: J(w,b), w, and b
but I don't know how to plot that yet, stay tuned. 