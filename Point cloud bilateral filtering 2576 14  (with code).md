#  Overview of the principle 

>  In the field of two-dimensional images, the bilateral filtering algorithm corrects the position of the current sampling center point by considering the distance from the center pixel to the neighbor pixel (one side) and the weight determined by the pixel brightness difference (the other side), so as to achieve a smooth filtering effect. At the same time, it will also selectively eliminate adjacent sampling points that are too "different" from the current sampling point, so as to achieve the purpose of maintaining the original characteristics. In the three-dimensional point cloud, we replace the bilateral weight with the distance weight of the current point and the neighbor point (one side) and the projection weight of the neighbor point along the normal vector of the current point (one side). As shown in the figure below: 

![avatar]( f31bafad3bdf4ae28ef86c6d115f4a04.png) 

>  Of which: 

![avatar]( 17efa486cfcb41ee8fd637b7d9e0eed1.png) 

>  The specific calculation process is as follows: 

![avatar]( fc926e4a50594aec96ba45c678f322a8.png) 

#  Implementation code 

>  BilateralFiltering.m 

 ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574034766
 ```  
#  III. Achieving results 

![avatar]( 572261a3c2bb4f7c832e01558cb23f00.png) 

>  It is obvious that the point cloud with previous noise has become much smoother, and this filtering method is still very effective. 

#  reference 

>  [1]https://blog.csdn.net/qq_33029733/article/details/106909683 [2]The Bilateral Filter for Point Clouds 

