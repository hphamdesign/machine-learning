<h1> Machine Learning - Assignment 3 </h1> 

<h2><a href="https://github.com/visualizedata/ml/tree/master/final_assignment_3/option_3">Option 3</a></h2>
<p>Work with data on food contamination to cluster incident descriptions into broader categories.<p>
  
<h2>My code modifications</h2>
In this iteration, I added 2 parameters to the CountVectorizer object:
<ul>
  <li> stop_words='english': I want to remove common English stop words ("a", "an", "the", "in", "on", "at", etc,) since they are not helpful and its removal will not affect the result.</li>
  <li> ngram_range=(1, 2): By considering both unigrams and bigrams, I want to capture both individual words and pairs of words, which can provide more context and potentially improve the performance of machine learning algorithms when working with text data.</li>
</ul>
<p> Next, I picked clusterVal values of 10, 25, 35, 45 to evaluate the clustering performance for 4 different numbers of clusters.</p>

<p>I also modified the value of n_clusters to i due to the utilization of a loop that iterates through a range of cluster numbers, starting from 1 and going up to clusterVal - 1. Within each loop iteration, a fresh instance of the KMeans object is generated, with n_clusters assigned to the current cluster number denoted by the loop variable i. By setting n_clusters to i, I can assess the clustering effectiveness for various cluster numbers automatically, without the need to manually adjust the value of n_clusters every time.</p>

<p>  Finally, I added the distortions to monitor the variations in distortion as the number of clusters increases. By analyzing the plot illustrating the relationship between the number of clusters and the distortion, I can pinpoint the elbow point and determine the most suitable number of clusters for the dataset. </p>
    
  
<h2> Plots </h2> 

<h4>Cluster 10</h4>

![image]()

<h4>Cluster 25</h4>

![image]()

<h4>Cluster 35</h4>

![image]()

<h4>Cluster 45</h4>

![image]()

<h4>Cluster 55</h4>

![image]()

<h2>My Assessment</h2>
<p>With n=10, there is a clear elbow around 3 clusters. However, in the output combined like (give examples from the output box) are categorizing unusually combination. Using greater value of n at 35,45 and 55; it is observed that the graph seems to be flattering around 25 and the output are categorized in a more reasonable manner</p>    

![image]()
