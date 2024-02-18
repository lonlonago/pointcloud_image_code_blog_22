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

