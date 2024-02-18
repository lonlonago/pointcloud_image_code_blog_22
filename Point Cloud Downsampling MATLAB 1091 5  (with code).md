>  Since I didn't have the downsampling functionality I wanted in MATLAB, I had to do it myself. 

#  First, specific ideas 

>  Drawing on the idea of voxel filter in PCL, a three-dimensional voxel grid is constructed according to the point cloud data we input and downsampled to achieve the filtering effect. In this process, the point contained in each voxel will eventually be replaced by the point closest to the center of the voxel. This method can ensure the shape characteristics of the point cloud while compressing the original point cloud data. 

#  Implementation code 

 ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574093747
 ```  
#  III. Achieving results 

![avatar]( 39be5ea4d1e24841a6c43bb9a8a89d21.png) 

