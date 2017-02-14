## PAMAE: PArallel k-Medoids clustering with high Accuracy and Efficiency

The k-medoids algorithm is one of the best-known clustering algorithms. Despite this, however, it is not as widely used for big data analytics as the k-means algorithm, mainly because of its high computational complexity. Many studies have attempted to solve the efficiency problem of the k-medoids algorithm, but all such studies have improved efficiency at the expense of accuracy. In this paper, we propose a novel parallel k-medoids algorithm, which we call **PAMAE**, that achieves both high accuracy and high efficiency. We identify two factors---"global search" and "entire data"---that are essential to achieving high accuracy, but are also very time-consuming if considered simultaneously. Thus, our key idea is to apply them individually through two phases: parallel seeding and parallel refinement, neither of which is costly. The first phase performs global search over sampled data, and the second phase performs local search over entire data. Our theoretical analysis proves that this serial execution of the two phases leads to an accurate solution that would be achieved by global search over entire data. In order to validate the merit of our approach, we implement PAMAE on Spark as well as Hadoop and conduct extensive experiments using various real-world and synthetic data sets on 12 Microsoft Azure machines (48 cores). The results show that PAMAE significantly outperforms most of recent parallel algorithms and, at the same time, produces a clustering quality as comparable as the previous most-accurate algorithm.

To compile this algorithm, you should import the external libary for spark and make jar file using IDE tools. You can download the library on this URL(http://spark.apache.org/). After that, you can run the algorithm using spark-submit script. 

Our four real datasets can be downloaded below links.<br />
1. Covertype <br />
https://dmlabdata.blob.core.windows.net/kmedoid/Covertype.csv<br />
2. Census1990 <br />
https://dmlabdata.blob.core.windows.net/kmedoid/Census1990.csv<br />
3. Cosmo50 - <br />
https://dmlabdata.blob.core.windows.net/kmedoid/Cosmo50.csv<br />
4. TeraClickLog150 <br />
https://dmlabdata.blob.core.windows.net/kmedoid/split_0.csv<br />
https://dmlabdata.blob.core.windows.net/kmedoid/split_2.csv<br />
https://dmlabdata.blob.core.windows.net/kmedoid/split_3.csv<br />
https://dmlabdata.blob.core.windows.net/kmedoid/split_4.csv<br />
https://dmlabdata.blob.core.windows.net/kmedoid/split_5.csv<br />            
