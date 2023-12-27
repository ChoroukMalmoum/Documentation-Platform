predict Function
===================

.. function:: predict(method="kmeans", n_clusters=4, scaled_df=None, df=None)

    The `predict` function encapsulates the process of cluster prediction, enabling users to infer cluster assignments for data points based on the specified clustering algorithm. By offering a versatile interface and integrating diverse methodologies, the function facilitates seamless cluster prediction, fostering exploration, and understanding of data structures and patterns.

    **Parameters**:

    - **method** (*str, optional*): Specifies the clustering algorithm to be employed for prediction. Valid options include "kmeans", "agglomerativeC", "dbscan", or "gmm". Default is "kmeans".
    
    - **n_clusters** (*int, optional*): The desired number of clusters for the selected clustering algorithm. Default is 4.
    
    - **scaled_df** (*DataFrame or array-like, optional*): The scaled dataset intended for cluster prediction, ensuring consistency and accuracy in results.
    
    - **df** (*DataFrame, optional*): The original dataset, retaining its intrinsic attributes and facilitating comprehensive analysis and visualization.

    **Returns**:

    A dataframe augmented with cluster labels derived from the specified clustering algorithm and a scatter plot visual representation depicting the distribution of data points within the predicted clusters, fostering intuitive comprehension and exploratory data analysis.


