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

