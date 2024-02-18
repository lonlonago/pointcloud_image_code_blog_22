#  I. Introduction 

>  Due to the differences in elevation between different ground objects, in order to remove the influence of terrain fluctuations on the elevation value of point cloud data, it is necessary to perform point cloud normalization processing according to the extracted ground points. This step is the foundation of many algorithms, which can improve the accuracy of subsequent point cloud classification or segmentation, as shown in the figure below. 

![avatar]( e27448da263847c1b4758a9de78a9547.png) 

#  Second, algorithm implementation 

##  2.1 Implementation ideas 

>  The process of normalization is actually relatively simple, traversing every non-ground point 

           p 

           i 

         p_i 

     Pi, find the distance 

           p 

           i 

         p_i 

     Pi nearest ground point 

           g 

           i 

         g_i 

     Gi, find the height difference between these two points, and use the calculated height difference as 

           p 

           i 

         p_i 

     The new elevation value of pi completes the normalization operation. 

##  2.2 Implementation code 

 ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574011699
 ```  
#  III. Achieving results 

>  Original data source 

![avatar]( feca807c4a9c4d70948c7f09a1bf64c0.png) 

![avatar]( 7bd240a952d64d6d81cc5e2746c37546.png) 

>  elevation normalization 

![avatar]( 62693548d2144f7c8dbfd4b524fb1028.png) 

![avatar]( 741aed3fa75f46b8a3d48701c3c3f158.png) 

![avatar]( b9cb955aa360433c85ae635245364358.png) 

