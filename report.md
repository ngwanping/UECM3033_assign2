UECM3033 Assignment #2 Report
========================================================

- Prepared by: Ng Wan Ping
- Tutorial Group: T2

--------------------------------------------------------

## Task 1 --  $LU$ Factorization or SOR method

The reports, codes and supporting documents are to be uploaded to Github at: 

https://github.com/ngwanping/UECM3033_assign2

Explain your selection criteria here.

Explain how you implement your `task1.py` here.

---------------------------------------------------------

## Task 2 -- SVD method and image compression

Put here your picture file (seaside.jpg)

![seaside.jpg](seaside.jpg)

How many non zero element in $\Sigma$?
There are 800 non zero elements in Sigma for three colors.
It mean all elements in Sigma of 3 colours are non zero.

Put here your lower and better resolution pictures. Explain how you generate
these pictures from `task2.py`.
![lower.png](lower.png)
![better.png](better.png)


First, create a self defined function named svd. Read the "seaside.jpg" image and assiged to img.
Then, compute the U,$\Sigma$ and V for for each of the red, green and blue matrices.
Use numpy function, count_nonzero to find number of non zero elememts in $\Sigma$ for red,green and blue colours respectively.
Create a new Sigma matrix by copying the each of original $\Sigma$ and keep the first n nonzero elememts while set all other none zero elements to zero by using numpy function zeros_like.
To construct a lower resolution matrix, change the dimension of $\Sigma$ from (800,1) to (800,1000)by using spicy function linalg.diagsvd,it is because the dimension of U is (800,800) and V is (1000,1009).
In order to use dot multiplication for new matrix,so the new matrix will be U*$\Sigma$ * V which is dimension of (800,1000).
Then, create and display the new resolution images.
All the steps above are in self defined function named svd.

To compress a lower resolution picture, call the svd function with input n=30.
To compress a better resolution picture, call the svd function with input n=200.


What is a sparse matrix?
A sparse matrix is a matrix with the most of the elememts are zero, mean it has larger number of zero values compared to nonzero.
In contrast,a matrix where many elements are nonzero is called dense, as the Sigma matrix we had in task 2.


-----------------------------------

last modified: 10 Marth 2016
