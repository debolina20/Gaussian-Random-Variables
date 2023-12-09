# Gaussian-Random-Variables

1. In this task, we will generate random vectors and perform some operations related to concepts we learned in class. Use a function to generate multi-variate Gaussian data given the parameters of the Gaussian, such as the python function mvnrnd. The function requires you to provide the mean vector and covariance matrix and the number of points you would like to sample from the distribution.
(a) Generate 1000 samples from a Gaussian distribution with the following parameters: µ =
[0, 0, 0], and Σ =
[
2 0 0
0 1.5 0
0 0 2.5
].
(b) Generate 1000 samples from a Gaussian distribution with the following parameters: µ =
[0, 0, 0], and Σ =
[
2 0.35 0.62
0.35 0.5 0.33
0.62 0.33 1
].
Plot the resulting scatter plots of the data you generate in parts (a) and (b) using the scatter3() function.

2. You will now implement your own function to carry out projection of random vectors onto principle components. Assume that the data are zero-mean. Implement the following in your custom function (call it ProjectData.m to avoid conflicts with built-in functions):
• Assume that the input to the function is a data matrix, X, of size d × n, comprising of n data samples, each a point (vector) in the d− dimensional Euclidean space, Rd. The output of the function will be a data matrix Y of size d2 × n, where d2 << d.
• Estimate the Covariance Matrix of the Data (you may use the built-in python function, cov for this).
• Perform the eigen-decomposition of the covariance matrix (you may use the built-in python function, eig for this). The eigenvector matrix you will get out of this is of size d × d.
• Ensure your eigenvectors and eigenvalues are sorted in descending order of eigenvalues - i.e., the first eigenvector corresponds to the largest eigenvalue, and so on...
• Your projection (transformation) matrix T is then obtained by selecting the first d2 columns of the eigenvector matrix, resulting in a transformation matrix T of size d × d2
• The transformation T : Rd → R d2 can be used to project data in the d-dimensional Euclidean space to a (lower) d2 dimensional subspace by the simple matrix operation Y = T′X.
Apply your transformation function to the synthetic Gaussian data generated in problem (1a) above, projecting the data from a 3-dimensional space to a 2-dimensional space. Estimate and report the covariance matrix of the projected data Y . Also visualize the 2-dimensional scatter plot of Y and compare it to the 3-D scatter plot obtained in (1a) and (1b).
