# cs540-homework-5-principal-component-analysis-solved
**TO GET THIS SOLUTION VISIT:** [CS540 Homework 5-Principal Component Analysis Solved](https://www.ankitcodinghub.com/product/cs540-hw5-principal-component-analysis-solved/)


---

📩 **If you need this solution or have special requests:** **Email:** ankitcoding@gmail.com  
📱 **WhatsApp:** +1 419 877 7882  
📄 **Get a quote instantly using this form:** [Ask Homework Questions](https://www.ankitcodinghub.com/services/ask-homework-questions/)

*We deliver fast, professional, and affordable academic help.*

---

<h2>Description</h2>



<div class="kk-star-ratings kksr-auto kksr-align-center kksr-valign-top" data-payload="{&quot;align&quot;:&quot;center&quot;,&quot;id&quot;:&quot;117936&quot;,&quot;slug&quot;:&quot;default&quot;,&quot;valign&quot;:&quot;top&quot;,&quot;ignore&quot;:&quot;&quot;,&quot;reference&quot;:&quot;auto&quot;,&quot;class&quot;:&quot;&quot;,&quot;count&quot;:&quot;2&quot;,&quot;legendonly&quot;:&quot;&quot;,&quot;readonly&quot;:&quot;&quot;,&quot;score&quot;:&quot;5&quot;,&quot;starsonly&quot;:&quot;&quot;,&quot;best&quot;:&quot;5&quot;,&quot;gap&quot;:&quot;4&quot;,&quot;greet&quot;:&quot;Rate this product&quot;,&quot;legend&quot;:&quot;5\/5 - (2 votes)&quot;,&quot;size&quot;:&quot;24&quot;,&quot;title&quot;:&quot;CS540  Homework 5-Principal Component Analysis Solved&quot;,&quot;width&quot;:&quot;138&quot;,&quot;_legend&quot;:&quot;{score}\/{best} - ({count} {votes})&quot;,&quot;font_factor&quot;:&quot;1.25&quot;}">

<div class="kksr-stars">

<div class="kksr-stars-inactive">
            <div class="kksr-star" data-star="1" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="2" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="3" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="4" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="5" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>

<div class="kksr-stars-active" style="width: 138px;">
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>
</div>


<div class="kksr-legend" style="font-size: 19.2px;">
            5/5 - (2 votes)    </div>
    </div>
Assignment Goals

Explore Principal Component Analysis (PCA) and the related Python packages Make pretty pictures 🙂

Summary

In this project, you’ll be implementing a handwriting analysis program using Principal Component Analysis (PCA).

We’ll walk you through the process step-by-step (at a high level).

Packages Needed for this Project

In this project, you’ll need the following packages:

Dataset

You’ll be using part of the MNIST dataset mnist.npy.

The dataset contains 2000 samples images, each of size 28*28. We will use n to refer to number of samples where n=2000. And d to refer to number of features for each sample which is d=28*28=784. We will only test your code using this data set. Here we’ll use to refer to the ith sample which would be a d dimension column vector.

Program Specification

Implement these six (6) Python functions to do PCA on our provided dataset, in a file called pca.py:

1. load_and_center_dataset(filename) — load the dataset from a provided .npy file, re-center it around the origin and return it as a NumPy array of floats

2. get_covariance(dataset) — calculate and return the covariance matrix of the dataset as a NumPy matrix (d x d array)

3. get_eig(S, m) — perform eigen decomposition on the covariance matrix S and return a diagonal matrix (NumPy array) with the largest m eigenvalues on the diagonal, and a matrix (NumPy array) with the corresponding eigenvectors as columns

4. get_eig_perc(S, perc) — similar to get_eig, but instead of returning the first m, return all eigenvectors that explains more than perc % of variance

5. project_image(image, U) — project each image into your m-dimensional space and return the new representation as a d x 1 NumPy array

6. display_image(orig, proj) — use matplotlib to display a visual representation of the original image and the projected image side-by-side

NOTE: your orig, proj, image and return value of project_image should have np.shape as (784,)

Load and Center the Dataset

First, if you haven’t, download our sample dataset to the machine you’re working on: mnist.npy.

Then, you should reshape the data to n*d (n, the number of images we’re analyzing, and d, the dimension of those images). Here we have d=28*28=784 (28 by 28 pixels).

This should give you an nxd dataset, where each row is an image feature vector of 784 pixels. Note this configuration for future calculations.

Your next step is to re-center this dataset around the origin. Re-centering is simply to subtract the

from each data point . This is defined as where

From now on, we will just use to refer to .

After you’ve implemented this function, it should work like this:

Its center isn’t exactly zero, but taking into account precision errors over 2000 arrays of 784 floats, it’s what we call Close Enough. (np.average(x) have absolute value below )

Find Covariance Matrix

As given in the notes, the covariance matrix is defined as (if you consider ith sample as a column vector)

as a row vector, then it is)

To calculate this, you’ll need a couple of tools from NumPy again:

The result of this function for our sample dataset should be a d*d (784×784) matrix.

Get m Largest Eigenvalues/Eigenvectors

You’ll never have to do eigen decomposition by hand again

(https://docs.scipy.org/doc/scipy/reference/generated/scipy.linalg.eigh.html) ! Use scipy.linalg.eigh() to help, particularly the optional eigvals argument.

We want the largest m eigenvalues of S.

Return the eigenvalues as a diagonal matrix, in descending order, and the corresponding eigenvectors as columns in a matrix.

To return more than one thing from a function in Python:

Get all Eigenvectors that Explain More than Certain % of Variance

We want all the eigenvalues that explain more than a certain percentage of variance. Let be an eigenvector and corresponding eigenvalue.

Then the percentage of variance explained is:

Return the eigenvalues as a diagonal matrix, in descending order, and the corresponding eigenvectors as columns in a matrix.

Project the Images

Given one of the images from your dataset and the results of your get_eig() function, create and return the projection of that image.

For any image xi, we project it into the m dimensional space span eigenvectors by:

where , and .

Visualize

We’ll be using matplotlib’s imshow

(https://matplotlib.org/3.1.3/api/_as_gen/matplotlib.pyplot.imshow.html) . First, make sure you have the matplotlib library (https://matplotlib.org/3.1.1/users/installing.html) , for creating figures.

Follow these steps to visualize your images:

1. Reshape the images to be 28×28 (you should have calculated them as 1d vectors of 784 numbers).

2. Create a figure with one row of two subplots

(https://matplotlib.org/api/_as_gen/matplotlib.pyplot.subplots.html) .

3. The first subplot (on the left) should be titled

(https://matplotlib.org/3.1.3/gallery/subplots_axes_and_figures/figure_title.html) “Original”, and the second (on the right) should be titled “Projection”.

4. Use imshow() with optional argument aspect=’equal’ and cmap=’gray’ to render the original image in the first subplot and the projection in the second subplot.

5. Use the return value of imshow() to create a colorbar

(https://matplotlib.org/3.1.0/gallery/color/colorbar_basics.html) for each image.

6. Render (https://matplotlib.org/api/_as_gen/matplotlib.pyplot.show.html) your plots!

NOTE: to plot image on CSL machines, you will need to save the plot to a file (cause it doesn’t have graphic interface)

1. add the following lines to the beginning of your code.

&gt;&gt;&gt; import matplotlib

&gt;&gt;&gt; matplotlib.use(‘Agg’)

2. indead of using plt.show() use plt.savefig(“filename.png”). (You should use plt.show() in your submission.)

Submission Notes

Please submit your files in a zip file named hw5_&lt;netid&gt;.zip, where you replace &lt;netid&gt; with your netID (your wisc.edu login). Inside your zip file, there should be only one file named: pca.py. Do not submit a Jupyter notebook .ipynb file.

Be sure to remove all debugging output before submission; your functions should run silently (except for the image rendering window). Failure to remove debugging output will be penalized (10pts).

Changelog

See below for updates to the assignment since the initial release

Added explanation for n and d in dataset section.

Updated to correct the diagonal flipped sample image.

Elaborate that is column vector.

Elaborate on the definition of covariance matrix as row vectors.

Add clarification that students will only be tested on mnist.npy

Added clarification on np.shape() of vectors

Added guide about how to test plot on CSL machines

Changed the CSL guide from jpg to png

Rubric

Criteria Ratings Pts

load_and_center_dataset 20.0 pts

get_covariance 15.0 pts

get_eig &amp; get_eig_perc 25.0 pts

project_image 15.0 pts

display_image 15.0 pts

image correctly formated 10.0 pts
