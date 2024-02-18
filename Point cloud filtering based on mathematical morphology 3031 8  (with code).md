#  I. Introduction 

>  The basic principle is to use the window template of the structural element (usually the filtered window) as the processing unit, and use the combination of expansion and corrosion in morphology to achieve the effect of filtering. 

>  The mathematical morphological operations in point cloud data are actually very similar to those on two-dimensional images. The pixels on the image have x, y, and luminance values. We often modify the luminance value of each pixel; while the points in the point cloud are (x, y, z). Therefore, it is easy to understand that the expansion in the point cloud is actually an operation on the z value of the point. 

>  In simple terms, the expansion operation in the point cloud is actually to increase the height of the point to the highest value in the field, while the corrosion operation is the opposite, that is, to reduce the height of the point to the lowest value in the neighborhood. Morphology-based point cloud filtering mainly uses the opening operation: first, the point cloud data is etched (take the low value), which can filter out non-ground points such as tree points smaller than the size of structural elements; then it is expanded (take the high value), which can restore the eroded edges such as buildings. Finally, according to the pre-set height difference threshold, the ground point and the non-ground point can be separated to achieve the desired point cloud filtering effect. 

#  Code implementation 

>  main.m 

 ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574023691
 ```  
>  corrosion.m 

 ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574023691
 ```  
>  inflation.m 

 ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574023691
 ```  
>  Improved version (later changed the code "~") 

 ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574023691
 ```  
#  III. Achieving results 

![avatar]( a35dbcb253584ffd88e53b5647556e3e.png) 

![avatar]( 645e5aca15e54392b159a9e5dfa3ef04.png) 

![avatar]( 09690b472aba4448b9315b1e4a5cc2b8.png) 

![avatar]( 132170baac5c450382a6640daa1d1bf1.png) 

![avatar]( 6dba3f0d2f6f45b9aecfa0a3d8846cd2.png) 

#  IV. Summary 

>  From the realization of the effect, the extraction of ground points and non-ground points, although there are a lot of errors (ground point error into non-ground points and non-ground point error into ground points), but the overall or to achieve the filtering effect, can extract most of the ground points "~". 

>  In addition, the above code also has the following problems: (1) The calculation efficiency is not high enough. This may be because I am not familiar with MATLAB, and I will improve the code later when I have time. Note: The improved version has been released, https://blog.csdn.net/dayuhaitang1/article/details/123486873 (2) The height difference threshold h_threshold is not set as said in the paper, but a threshold is set casually, so the follow-up needs to be more in-depth research "_". 

>  Reference: [1] Research on information extraction of road lights and street trees in vehicle LiDAR point cloud _ Zhang Xitong 

