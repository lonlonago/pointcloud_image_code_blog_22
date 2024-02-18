#  I. Introduction 

>  Previously, the normalization operation was based on the ground point, but from some literature, it was seen that the normalization operation could be performed based on the grid, which was very interesting, so I recorded it. 

#  Second, algorithm implementation 

##  2.1 Ideas 

>  (1) First, the point cloud is gridded in the horizontal direction. (2) The lowest point in each grid is used as the reference point, that is, the ground point, and the height difference between other points in the grid and this point is calculated. (3) Finally, the elevations of the points in the grid are changed to the high difference with the reference point to realize the normalization of the data. 

##  2.2 Implementation code 

 ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574018413
 ```  
#  III. Achieving results 

>  Original data source 

![avatar]( b99e6ca180744519bb2e071e35e893d7.png) 

>  normalized data 

![avatar]( 9e881f39f0cf4af0831bfeecd708ba90.png) 

#  References 

>  [1] An automatic power line extraction method based on airborne LiDAR point cloud 

