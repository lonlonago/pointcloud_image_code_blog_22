#  Overview of the principle 

>  When learning the calculation of normal vector, I once said that the PCA algorithm was originally a method for evaluating curvature. Of course, there are many ways to represent the curvature of a point, but generally they all need to use triangular grids for representation. The author in the literature [1] defined Gaussian curvature 

          K 

         K 

     K and mean curvature 

          H 

         H 

     H represents the degree of curvature of a smooth surface. However, since many expressions of curvature are sensitive to noise, subsequent scholars generally use the eigenvalues of the covariance of the point neighborhood to approximate the curvature of the point. The formula is as follows: 

![avatar]( b9c811ffd8714ba88736aadcfcd6bcae.png) 

#  Code implementation 

>  curvatureV1.m 

 ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574086911
 ```  
#  III. Achieving results 

![avatar]( 6e57cdf0b92d4891bde1f09a6176ddde.png) 

#  References 

>  [1] Optimizing 3D triangulations using discrete curvature analysis. [2] Semantic 3D Object Maps for EverydayManipulation in Human Living Environments 

