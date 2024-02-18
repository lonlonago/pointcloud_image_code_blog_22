#  interaction problem 

"PCL + QT" version interaction (updating) 

#  Configuration issues: 

Summary of environment configuration issues for each version of "PCL + QT" (completed) 

#  The latest addition: "QT + PCL" supplement 

"QT + PCL" supplement - add point cloud tree control (completed) 

"QT + PCL" supplement - point cloud operation after adding tree controls (filtering, registration as an example (completed) 

"QT + PCL" Supplement - Point Cloud Perspective Setup (Completed) 

#  First, the basic operation of "QT + PCL Chapter 1" 

The reading display of point cloud in 1.1 qt (completed) 

Point cloud file saving in 1.2 qt (completed) 

#  Second, "QT + PCL Chapter II" point cloud display 

Software background settings in 2.1 qt (completed) 

2.2 qt midpoint cloud rendering settings (completed) 

Point cloud color setting in 2.3 qt (completed) 

Adjust the point cloud size setting in 2.4 qt (completed) 

#  3. "QT + PCL Chapter 3" Point Cloud Filtering 

Add voxel filtering to 3.1 qt (completed) 

Add approximate voxels to 3.2 qt (completed) 

Adding uniform sampling in 3.3 qt (completed) 

Added fixed point sampling in 3.4 qt (completed) 

Adding gridmin filtering to 3.5 qt (completed) 

Add improved voxels to 3.6 qt 

Adding statistical filtering to 3.7 qt (completed) 

Added radius filtering in 3.8 qt (completed) 

Adding Gaussian filtering to 3.9 qt (completed) 

Add bilateral filtering in 3.10 qt 

Add fast bilateral in 3.11 qt 

Add projection filtering to 3.12 qt (completed) 

Add median filtering in 3.13 qt 

Add pass-through filtering to 3.14 qt (completed) 

Add conditional filtering to 3.15 qt (completed) 

Add morphological filtering to 3.16 qt 

Add upsampling filter in 3.17 qt (completed) 

#  IV. Key Points of "QT + PCL Chapter IV" Point Cloud 

Add the key point ISS in 4.1 qt (completed) 

4.2 Added key point Harris to qt (completed) 

Added key point SIFT in 4.3 qt (completed) 

#  Point cloud characteristics of "QT + PCL Chapter 5" 

Adding point cloud normals to 5.1 qt 

5.2 Qt to add feature PFH 

 5.3 qt add point cloud feature FPFH 

Adding point cloud feature RSD in 5.4 qt 

Adding point cloud feature 3DSC in 5.5 qt 

Adding point cloud feature USC in 5.6 qt 

5.7 Add point cloud feature SHOT in qt 

5.8 qt add point cloud feature SPinImage 

5.9 qt add point cloud feature RIFT 

Adding point cloud feature NARF in 5.10 qt 

5.11 qt add point cloud feature RopS 

Adding point cloud feature VFH in 5.12 qt 

Adding point cloud feature CVFH in 5.13 qt 

5.14 Qt add point cloud feature OUR_CVFH 

Adding point cloud feature ESF in 5.15 qt 

Adding point cloud feature GFPFH in 5.16 qt 

5.17 qt add point cloud feature GRSD 

#  "QT + PCL Chapter 6" Point Cloud Registration 

Added icp registration series 1 to 6.1 qt (completed) 

Added icp registration series 2 to 6.2 qt (completed) 

Added icp registration series 3 to 6.3 qt (completed) 

Added icp registration series four to 6.4 qt (completed) 

6.5 QT Muscle Building ICP Registration Series 5 (Completed) 

Added icp registration series six to 6.6 qt (completed) 

Added 4pcs series to 6.7 qt with a 4pcs implementation (completed) 

Added 4pcs series two k4pcs to 6.8 qt (completed) 

Added 4pcs series three super4pcs implementation in 6.8 qt (completed) 

Added feature registration series 1 in 6.9 qt 

Added feature registration series 2 in 6.10 qt 

Added feature registration series 3 in 6.11 qt 

Added feature registration series 4 in 6.12 qt 

Added feature registration series 5 in 6.13 qt 

Added feature registration series 6 in 6.14 qt 

Added point cloud registration NDT in 6.15 qt (completed) 

6.16 Point Cloud Registration Advanced - GROR Registration (Completed) 

#  "QT + PCL Chapter 7" Point Cloud Segmentation 

Added point cloud segmentation - straight line segmentation in 7.1 qt (completed) 

7.2 Qt added point cloud segmentation - circular segmentation (completed) 

Added point cloud segmentation-plane segmentation in 7.3 qt (completed) 

Added point cloud segmentation-cylindrical segmentation in 7.4 qt (completed) 

Added point cloud segmentation-Euclidean clustering in 7.5 qt (completed) 

Adding point cloud segmentation in 7.6 qt - regional growth (completed) 

Adding point cloud segmentation in 7.7 qt - area growth 2 

Add point cloud segmentation-super voxel segmentation in 7.8 qt 

7.9 qt to add point cloud segmentation - LCCP (completed) 

Add point cloud segmentation-CPC in 7.10 qt (completed) 

7.11 Qt added point cloud segmentation - minimum cut 

Add point cloud segmentation in 7.12 qt - morphological segmentation 

Add point cloud segmentation in 7.13 qt - progressive morphological segmentation 

#  8. "QT + PCL Chapter 8" Point Cloud Recognition 

Add point cloud recognition in 8.1 qt 

#  "QT + PCL Chapter 9" Point Cloud Reconstruction 

Added Point Cloud Reconstruction Series 1 in 9.1 qt - Greedy Triangulation (Completed) 

Added Point Cloud Reconstruction Series 2-Poisson Reconstruction in 9.2 qt (completed) 

Added point cloud reconstruction series 3-moving cube in 9.3 qt 



--------------------------------------------------------------------------------

#  I. Introduction 

>  According to the plane extracted by the RANSAC algorithm, the segmentation results are optimized by using the normal vector between the facets and the Euclidean distance discrimination. 

#  Implementation code 

>  MergePlaneV1.m 

 ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574072202
 ```  
#  III. Achieving results 

![avatar]( b3e04cee61d94f9c827b848575ce771f.png) 

#  References 

>  [1] Improved RANSAC point cloud segmentation algorithm and its application 



--------------------------------------------------------------------------------

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



--------------------------------------------------------------------------------

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



--------------------------------------------------------------------------------

#  I. Introduction 

>  There are many clustering algorithms in MATLAB. Here are a few of the clustering algorithms I have used before, mainly including: dbscan, k-means, and fcm clustering algorithms. 

#  II. Relevant codes 

>  DBSCAN and k-means clustering have been introduced in previous articles, so I won't say more here. For details, you can check the point cloud K-Means clustering algorithm and the point cloud DBSCAN clustering algorithm. Finally, about the FCM algorithm, in simple terms, the algorithm is based on the basic principle of least squares, and uses repeated iterations to continuously improve the objective function to achieve a reasonable classification of the dataset. Its essence is to minimize the square error. It is different from the distance principle of kmeans clustering. It introduces the idea of similarity and adds an uncertainty to cluster selection (the origin of "fuzzy"), so it has stronger robustness than kmeans clustering. 

>  The setting of relevant parameters is not introduced here. MATLAB's official website is very detailed, or if you select the function name in MATLAB and press F1, there will be more detailed help documents. The specific code demonstration is as follows: 

>  Cluster.m 

 ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574069235
 ```  
#  III. Achieving results 

![avatar]( 0e8141261b944261a84e3a45c835d421.png) 

>  In addition to these clustering methods, MATLAB's point cloud tool library also includes other clustering methods, such as European-style clustering pcsegdist, etc., which will not be discussed here. 

#  reference 

>  [1] https://ww2.mathworks.cn/help/fuzzy/fcm.html?requestedDomain=cn [2] https://ww2.mathworks.cn/help/stats/kmeans.html?s_tid=doc_ta [3] https://ww2.mathworks.cn/help/stats/dbscan.html?s_tid=doc_ta [4] Research on the extraction accuracy of the center of the plane target by FCM clustering algorithm 



--------------------------------------------------------------------------------

#  Overview of the principle 

>  According to different elevation values, each point is assigned a different color. Here, the color band in MATLAB will be used to complete this function. 

#  Implementation code 

>  ElevationRendering.m 

 ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574098072
 ```  
#  III. Achieving results 

![avatar]( f54edd03652e4ef4b91fe68cd203d217.png) 



--------------------------------------------------------------------------------

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



--------------------------------------------------------------------------------

#  I. Introduction 

![avatar]( 0c5915c1442b460fbfd870900a5cd19d.png) 

#  Code implementation 

>  NormalCurvature.m 

 ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574078520
 ```  
#  III. Achieving results 

![avatar]( 8cf88a6d1d5e4461aa7dad219ce8ac73.png) 

#  reference 

>  [1] An Improved ICP Algorithm Based on Gaussian Curvature 



--------------------------------------------------------------------------------

#  I. Introduction 

>  Because I also feel curious about the depth image, I simply use the orthographic projection method to generate a depth image to see the effect. The depth value here uses the difference of the z value (height difference). The specific code and effect are as follows. 

#  Second, the image generation code 

Here the point cloud is projected onto the XOY plane, using the elevation difference as the depth value. 

 ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 202402030957404382
 ```  
#  III. Achieving results 

![avatar]( 2c1a423b7175481f91c0710578968d3e.png) 

![avatar]( 8e73367b25a347e69f314fd42cf59f7a.png) 



--------------------------------------------------------------------------------

#  I. Introduction 

>  I have used the generating depth image function in PCL before, and I want to use MATLAB to achieve a similar function. The whole process is a sampling process of rotating horizontal and vertical angles, as shown in the figure below (for details, you can also refer to the depth image to point cloud data (lidar data)). The final result can be determined by the row number and column number. The specific calculation process can be read in the code. 

![avatar]( 9b7c37c0ff354de1b38c0caabea9b180.png) 

#  Second, the image generation code 

 ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574012268
 ```  
#  III. Achieving results 

![avatar]( 0728732e4153465095faff549452f10d.png) 

![avatar]( 69c2612f64eb4a5983a377ab7daec23c.png) 

#  reference 

>  [1]https://pcl.readthedocs.io/projects/tutorials/en/latest/range_image_creation.html#range-image-creation 



--------------------------------------------------------------------------------

#  DBSCAN algorithm 

>  DBSCAN algorithm, the full name is "Density-Based Spatial Clustering of Applications with Node", which is "density-based clustering". This kind of algorithm assumes that the cluster structure can be determined by the tightness of the sample distribution, examines the continuity between samples from the perspective of sample density, and continuously expands the clustering cluster based on the connectable samples to obtain the final clustering result. 

As a well-known density clustering algorithm, the DBSCAN algorithm uses the neighborhood parameter (Distance, MinPts) to describe the tightness of the sample distribution. Before we start, we must first understand the following concepts: 

![avatar]( 20200501224404315.png) 

>  Core objects: x1, x2, which is the point that satisfies the condition of the neighborhood parameter (Distance, MinPts). Density direct: x2 is direct from x1 density. Density reachable: x3 is reachable from x1 density. Density connected: x3 is connected to x4 density. For specific definitions, please refer to the book "Machine Learning". I will briefly explain these concepts here. 

#  Second, the algorithm steps 

>  1. Initialize the core object and record its adjacent points. Loop through each data point, record other data points in the neighborhood of each data point < = Distance parameter (distance parameter), and determine whether the number of adjacent points that meet the distance parameter > = MinPts parameter (number of points parameter). If it meets the addition, add the data point to the collection of core objects. 2. Clustering. First select a core object in the dataset as the "seed", and then start from this to find out all the sample sets of its density to generate the corresponding cluster cluster until all the core objects have been visited. 

#  Third, the code implementation effect 

Original data source: 

![avatar]( 20200501092319862.png) 

 main.cpp： 

 ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574025496
 ```  
Point3.h： 

 ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574025496
 ```  
PointDataSource.h： 

 ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574025496
 ```  
DBSCAN.h： 

 ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574025496
 ```  
Processing effect: 

![avatar]( 20200501235258431.png) 

#  IV. Summary 

During the course of this experiment, there are several points to be noted: 

>  1. The use of kdtree. Since the DBSCAN algorithm in this experiment involves the radius nearest neighbor query of the point, the first time I used the traversal method to query the calculation, it would cause the program to run for too long and could not calculate the result. Therefore, I used the data structure of kdtree in PCL. Although the effect was handled well, the program still took a long time to run (about 6 minutes at a radius of 0.4). There are some jokes here. I have been running the program in Debug mode before, which made the running time very slow (and made me complain for a long time "_"). After that, I tried it in release mode, and the running time was immediately shortened to about 20s. 2. Recursive method. The recursive method can also achieve the depth-first search clustering effect of data points, but when the amount of data is too large (> 10000), the program will start to report errors, because the depth of recursion reaches the limit of the computer, so I use the "while + queue" method instead of the recursive method to avoid the problem of excessive recursive depth. If you are interested in recursive clustering of DBSCAN algorithm, you can read this document: DBSCAN Recursive Clustering. 

>  Reference: "machine learning" "DBSCAN recursive clustering" 



--------------------------------------------------------------------------------

#  I. Introduction 

>  The relevant content of this method has been detailed in the previous article (point cloud DBSCAN clustering algorithm (C++)), and it will not be repeated here. 

#  Implementation code 

>  DBSCAN.m 

 ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574051053
 ```  
>  main.m 

 ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574051053
 ```  
#  III. Achieving results 

![avatar]( 1e84a5fbfc9b47d09641d650125b4dd3.png) 

#  reference 

>  [1] Point cloud DBSCAN clustering algorithm (C++) 



--------------------------------------------------------------------------------

#  effect display 

![avatar]( 3b4e77d2052a43ac917e3af21d61f9e3.gif) 

#  I. Introduction 

#  Code 

##  2.1 Read the H5 model and convert it to Open3D read. 

Read h5 

 ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574067096
 ```  
Change to open3d read 

 ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574067096
 ```  
##  2.2 The problem of graphicsView perspective 

![avatar]( 9591bd43b5244acfa81a5bf4a5d8ff3d.png) 

 Here, as reminded by the comment area, is changed to the following:  

 ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574067096
 ```  
#  III. Overall code 

##  3.1 main.py 

 ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574067096
 ```  
##  3.2 registration_dcp_rc.py code 

 ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574067096
 ```  
#  IV. Attention 

##  4.1 Model problems 

##  4.2 Data issues 

![avatar]( 31b3b107726a45b485057ec9a08fdd38.png) 

 over!!! 



--------------------------------------------------------------------------------

Sample demo sample download 

#  First, point cloud foundation 

1.1 Point cloud read, save, display 1.2 Point cloud read, save, display - 2 

#  Point cloud filtering 

2.1 point cloud voxel sampling 2.2 point cloud uniform sampling 2.3 point cloud random sampling 2.4 point cloud radius filtering 2.5 point cloud statistical filtering 2.6 point cloud FPS sampling 

#  Point cloud registration 

3.1 Point cloud fast global registration 3.2 Point cloud DCP network registration 3.3 Point cloud ICP point-to-point registration 

#  Point cloud segmentation 

4.1 Point Cloud Euclidean Clustering 

#  Point cloud reconstruction 

#  Six, grid processing 

#  Advanced processing 



--------------------------------------------------------------------------------

>  Since I didn't have the downsampling functionality I wanted in MATLAB, I had to do it myself. 

#  First, specific ideas 

>  Drawing on the idea of voxel filter in PCL, a three-dimensional voxel grid is constructed according to the point cloud data we input and downsampled to achieve the filtering effect. In this process, the point contained in each voxel will eventually be replaced by the point closest to the center of the voxel. This method can ensure the shape characteristics of the point cloud while compressing the original point cloud data. 

#  Implementation code 

 ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574093747
 ```  
#  III. Achieving results 

![avatar]( 39be5ea4d1e24841a6c43bb9a8a89d21.png) 



--------------------------------------------------------------------------------

#  I. Introduction 

>  In a two-dimensional plane, the extremum points in any direction of the point cloud need to be determined by the extremum of the polynomial ax + by. Here a and b can be any real numbers. If we want to obtain the extremum points in the upper left, upper left, upper right, lower left, and lower right directions, we actually take a and b as 0 and ± 1. I feel that this way of obtaining the extremum points is very interesting, so I implemented it. 

#  Implementation code 

>  ExtrectConvexExtreme.m 

 ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574028977
 ```  
#  III. Achieving results 

![avatar]( b6cd66b0f86149c08652d05aeacb4871.png) 

![avatar]( 6876578aebce40f7b6fce090a388d8fb.png) 

#  References 

>  [1] Improved fast calculation method of convex hull in two-dimensional point set 



--------------------------------------------------------------------------------

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



--------------------------------------------------------------------------------

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



--------------------------------------------------------------------------------

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



--------------------------------------------------------------------------------

#  First, the idea 

>  The initial method uses real data for calculation. In fact, you can learn from the idea of pointers in C language. You only need to record the index of each point, and you don't need the x, y, and z of each point to participate in the calculation. In addition, you have learned some problems with the syntax performance in MATLAB, and the effect will be much better than before. About 200,000 points can complete the expansion and corrosion operations in a very short time. 

#  Code 

>  main.m 

 ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574041314
 ```  
#  III. Achieving results 

>  Original data source 

![avatar]( d9881e0da2a24b3aa6713d52a44d349e.png) 

>  Run effect: 

![avatar]( c22c1dea6b8f4e8bbfbb9b47c3338294.png) 

![avatar]( dd0ef1d3b41b47e99ceb36cee64f394d.png) 

![avatar]( 0424741ac89c46f7a3a95b9375e4e0d9.png) 

![avatar]( 192df6e862754a329b53e55a21200d74.png) 



--------------------------------------------------------------------------------

