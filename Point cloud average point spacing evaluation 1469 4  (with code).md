Because I had seen a method to evaluate the average point spacing of a point cloud object before, I deliberately implemented it. 

#  First, specific ideas 

>  The idea is very simple. First, get the nearest point of each point in the point cloud, then calculate the distance from that point to its nearest point, add this distance, and finally divide by the number of points to get the average distance of the point cloud. After that, I used the sub-sampling function in CloudCompare to test it, and there is a certain effect, so record it. 

#  Code implementation 

>  PointsAverageSpacing.m 

 ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574045774
 ```  
#  III. Achieving results 

>  The test process first uses the sub-sampling function in CloudCompare. For details, please refer to: https://blog.csdn.net/dayuhaitang1/article/details/106698688, use the minimum distance from 0.01 to 0.1m, and then use the above method to calculate the average point spacing of the point cloud. The results are as follows. 

![avatar]( 4d6aaf99660c4d429d9a1b0fb03c977a.png) 

![avatar]( 9ac6a76f75dc47509548c18957cc06f9.png) 

