OptimalNumberOfClusters Function
====================================


.. function:: OptimalNumberOfClusters(method="elbow", scaled_df=None, k_min=2, k_max=7)

    The `OptimalNumberOfClusters` function is designed as a comprehensive tool for determining the ideal number of clusters in a dataset. It amalgamates multiple methodologies to provide users with a versatile and informed approach to cluster selection.

    **Parameters**:

    - **method** (*str, optional*): Specifies the method to use for cluster determination. Options include "elbow", "silhouette", or "dendrogram". Default is "elbow".
    
    - **scaled_df** (*DataFrame or array-like, optional*): The dataset subjected to clustering analysis, preprocessed and scaled for optimal results.
    
    - **k_min** (*int, optional*): The minimum number of clusters to consider during analysis. Default is 2.
    
    - **k_max** (*int, optional*): The maximum number of clusters to consider during analysis. Default is 7.

    **Returns**:

    A string containing a summary of the optimal number of clusters identified by the chosen methodology, accompanied by relevant evaluation metrics.
