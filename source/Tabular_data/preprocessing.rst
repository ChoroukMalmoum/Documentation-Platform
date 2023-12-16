Data Preprocessing
++++++++++++++++++

Data preprocessing is a critical step in preparing raw datasets for analysis and modeling. It involves cleaning the data to ensure its quality, consistency, and suitability for further processing. In our application, data preprocessing encompasses a range of tasks, including cleaning, transformation, and Exploratory Data Analysis (EDA).

1. **Cleaning:**
------------------------
    a. **Handling Outliers:**
       Our application provides options for handling outliers, allowing users to choose between automated methods or customized approaches. Two primary strategies are available:

       - **Z-Score Method:**
         Suited for datasets with a normal distribution, this method identifies outliers based on their deviation from the mean in terms of standard deviations using the ``z_threshold`` .

       - **IQR Method:**
         Ideal for datasets with skewed distributions, this method uses the Interquartile Range (IQR) to detect and manage outliers using the ``iqr_multiplier``.

         Handle missing data in a DataFrame with the following parameters:
        - **method (str):** ``auto``, ``z-score``, or ``iqr``.
        - **z_threshold (float):** Z-score threshold for outlier removal.
        - **iqr_multiplier (float):** Multiplier for IQR-based outlier removal.
        - **Returns:** DataFrame with outliers handled according to the specified method.
       
       .. note::
        - If the specified method is set to ``auto``, the codeè calculates the skewness of the data in the given column using the skew() function. Skewness is a measure of the asymmetry of the data distribution.  If the skewness is less than 1, it assumes a normal distribution ('z-score'); otherwise, it assumes a skewed distribution ('iqr').
        - Refer to the `Pandas.DataFrame.skew documentation <https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.skew.html>`_ for more details on the ``skew()`` function. 
    b. **Handling Missing Data:**
       Dealing with missing data is a common challenge in real-world datasets. Our application offers flexibility in handling missing values, giving users the choice to:

       - **Delete Missing Data:**
         Users can opt to remove rows or columns containing missing values.

       - **Impute Missing Values:**
         Imputation methods include filling missing values with the mean, median, or a user-specified constant. Alternatively, users can leverage K-Nearest Neighbors (KNN) imputation for a more sophisticated approach.

         Additional Information for Handling Missing Data:
         Handle missing data in a DataFrame with the following parameters:

         - **method (str):** ``drop`` to drop rows or columns, 'impute' to fill missing values. The provided impute methods are:  ``mean``, ``median`` and ``constant``
         - **threshold (float):** Threshold for dropping rows or columns based on missing values percentage.
         - **imputation_method (str):** Method for imputation when 'method' is set to 'impute'.
           Options: 'mean', 'median', 'constant', 'knn'.
         - **constant_value:** Constant value to fill missing values if 'imputation_method' is set to 'constant'.
         - **k_neighbors (int):** Number of neighbors to consider for KNN imputation.

         - **Returns:**
           DataFrame with missing values handled according to the specified method.

       - Refer to the `scikit-learn SimpleImputer documentation <https://scikit-learn.org/stable/modules/generated/sklearn.impute.SimpleImputer.html>`_ for more details on the ``mean``, ``median`` and ``constant`` imputation methods.
       - Refer to the `scikit-learn KNNImputer documentation <https://scikit-learn.org/stable/modules/generated/sklearn.impute.KNNImputer.html>`_ for more details on the ``Knn`` imputation method.
       - Refer to the `Pandas.DataFrame.dropna documentation <https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.dropna.html>`_ for more details on the ``drop`` rows or columns method.



1. **Handling Structural Errors:**   
------------------------------------
   - **Unstructured date:**
     In the context of data formation adhering to the ISO 8601 standard for date and time-related data.
    .. note::
        ISO 8601 is an international standard covering the worldwide exchange and communication of date and time-related data. It is maintained by the International Organization for Standardization (ISO). 
        ISO 8601 applies to these representations and formats: dates, in the Gregorian calendar (including the proleptic Gregorian calendar); times, based on the 24-hour timekeeping system, with optional UTC offset; time intervals; and combinations thereof.

   - **Removing White Spaces:**
     Trimming unnecessary spaces ensures data uniformity and consistency.

   - **Converting to Lowercase:**
     Standardizing text data by converting it to lowercase minimizes errors due to case variations.
   - **Returns:** DataFrame with Structural Errors handled.
     
 

3. **Data Transformation:**
------------------------------------
    In addition to cleaning, data transformation is a crucial step in refining and enhancing datasets for analytical purposes. Our application provides a suite of transformation functionalities to empower users in shaping and optimizing their data.

    a. **Feature Selection:**

        Personalise your dataset to focus on the most relevant features. Our application supports Principal Component Analysis (PCA) for feature selection, allowing users to:

        - Specify the number of desired features.
        - Optionally choose specific features to retain.
        - Option for an automated mode for streamlined selection.
        - Refer to the `sklearn.decomposition.PCA documentation <https://scikit-learn.org/stable/modules/generated/sklearn.decomposition.PCA.html>`_ for more details on the ``PCA`` method.


    b. **Aggregation and Grouping:**

        Aggregate and group data based on specific criteria to derive meaningful insights. The application offers a flexible method for aggregating data, allowing users to:

        - Identify grouping columns.
        - Specify aggregation functions for each column: max, min, sum, mean, median, std, numique, first and last.
        - Refer to the `pandas.DataFrame.agg documentation <https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.agg.html>`_ for more details on the ``Aggregation`` method.

        This functionality facilitates the creation of summarized datasets for more efficient analysis.

    c. **Replace Excess Categories with "Other":**

        Address categorical data challenges by replacing less common values. Our application provides the option to:

        - Select columns for replacement.
        - Specify the number of top values to retain (default is 3).
        - Automatically replace excess categories with 'other' for improved data clarity.

    d. **Feature Scaling:**

        Standardize or normalize numerical features for improved model performance. The application supports:

        - Scaling specific numerical features. If the list of specific features to scales is not provided, all numerical columns will be scaled.
        - Choosing between standardization and min-max scaling methods.
        - Refer to the `sklearn.preprocessing.StandardScaler documentation <https://scikit-learn.org/stable/modules/generated/sklearn.preprocessing.StandardScaler.html>`_ for more details on the ``Standardization`` method.
        - Refer to the `sklearn.preprocessing.MinMaxScaler documentation <https://scikit-learn.org/stable/modules/generated/sklearn.preprocessing.MinMaxScaler.html>`_ for more details on the ``Minmax`` method.

        This ensures that numerical features contribute uniformly to the analysis.

    e. **Merge Datasets:**

        Combine datasets seamlessly based on user-specified columns and merge type. Users can:

        - Select datasets to merge.
        - Choose the merge type ('left', 'right', 'inner', 'outer').
        - Refer to the `pandas.DataFrame.merge documentation <https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.merge.html>`_ for more details on the ``merge`` method.

        This facilitates the integration of disparate datasets for a comprehensive analysis.

    These transformation capabilities empower users to mold their data to meet specific analytical requirements, enhancing the overall effectiveness of downstream analyses.
