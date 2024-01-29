Test Function
===============

.. function:: test(n_clusters = 2, scaled_df=None, df=None, eps_dbscan=0.5, min_samples_dbscan=4, metric_dbscan='euclidean',clusters_column='')

    The `test` function serves as a comprehensive platform for comparative analysis of various clustering algorithms. By providing multiple clustering techniques and integrating them into a unified framework, the function facilitates empirical evaluations, enabling users to discern algorithmic nuances, performance characteristics, and cluster structures.

    **Parameters**:

    - **n_clusters** (*int, optional*): The desired number of clusters for clustering algorithms. Default is 2.
    
    - **scaled_df** (*DataFrame, required*): The dataset subjected to clustering analysis, preprocessed and scaled for optimal results.
    
    - **df** (*DataFrame, required*): The original dataset, preserving its intrinsic attributes and facilitating comprehensive analysis and visualization.
    
    - **eps_dbscan** (*float, optional*): The maximum distance between two samples for one to be considered as in the neighborhood of the other in DBSCAN clustering. Default is 0.5.
    
    - **min_samples_dbscan** (*int, optional*): The number of samples in a neighborhood for a point to be considered as a core point in DBSCAN clustering. Default is 4.
    
    - **metric_dbscan** (*str, optional*): The distance metric to use in DBSCAN clustering. Default is 'euclidean'.
    
    - **clusters_column** (*str, required*): The column containing the clusters.

    **Returns**:

    A dataframe enriched with cluster labels derived from each of the tested clustering algorithms and a multi-plot visualization showcasing clustering outcomes, fostering intuitive interpretation and comparative assessment. and a scores_df : a dataframe containing the scores for each clustering method, specifically the F1 and Accuracy.


.. note::
  For examples of usage, refer to the `Google Colab Notebook <https://colab.research.google.com/drive/1H5MSjPEfX5ZLpY13rGExV5jFHgFrepyv?usp=sharing>`