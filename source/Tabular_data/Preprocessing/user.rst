Data Preprocessing
++++++++++++++++++

Data preprocessing is a critical step in preparing raw datasets for analysis and modeling. It involves cleaning the data to ensure its quality, consistency, and suitability for further processing. In our application, data preprocessing encompasses a range of tasks, including cleaning, transformation, and Exploratory Data Analysis (EDA).

**Cleaning**
---------------

a. **Handling Outliers**
==============================
       The `handle_outliers <outliers.html>`_ method offers users 3 options for managing outliers. Users can start by selecting the specific column for outlier removal and then choose between automated methods or personalized approaches. Two primary strategies are available:

       - **Z-Score Method:**
         Suited for datasets with a normal distribution, this method identifies outliers based on their deviation from the mean in terms of standard deviations using the ``z_threshold`` .

       - **IQR Method:**
         Ideal for datasets with skewed distributions, this method uses the Interquartile Range (IQR) to detect and manage outliers using the ``iqr_multiplier``.

       - The class can detect the distribution type if 'auto' is selected and then apply one of the previous methods.

b. **Handling Missing Data**
===================================
       The `handle_missing_data <missing_values.html>`_ method offers flexibility in handling missing values, giving users the choice to:

       - **Delete Missing Data:**
         Users can opt to remove rows or columns containing missing values.

       - **Impute Missing Values:**
         Imputation methods include filling missing values with the mean, median, or a user-specified constant. Alternatively, users can use K-Nearest Neighbors (KNN) imputation.


**Handling Structural Errors**   
----------------------------------
  
a. **Basic unstructured data**
==================================
      The `fix_structural_errors <structural_errors.html>`_ method addresses basic structural errors:

     - **Removing White Spaces:**
       Trimming unnecessary spaces ensures data uniformity and consistency.

     - **Converting to Lowercase:**
       Standardizing text data by converting it to lowercase minimizes errors due to case variations.
    
b. **Unstructured date format**
====================================
     The `convert_to_iso8601 <convert_to_iso8601.html>`_ method addresses dates structural errors. In the context of data formation adhering to the ISO 8601 standard for date and time-related data.
    .. note::
        ISO 8601 is an international standard covering the worldwide exchange and communication of date and time-related data. It is maintained by the International Organization for Standardization (ISO). 
        ISO 8601 applies to these representations and formats: dates, in the Gregorian calendar (including the proleptic Gregorian calendar); times, based on the 24-hour timekeeping system, with optional UTC offset; time intervals; and combinations thereof.
   
 

**Data Transformation**
-------------------------

    In addition to cleaning, data transformation is a crucial step in refining and enhancing datasets for analytical purposes. Our application provides a suite of transformation functionalities to empower users in shaping and optimizing their data.

a. **Feature Selection**
==============================
        The `scale_features <Feature_Selection.html>`_ method supports Principal Component Analysis (PCA) for feature selection, allowing users to:
        - Specify the number of desired features.
        - Optionally choose specific features to retain.
        - Option for an automated mode for streamlined selection.
        


b. **Aggregation and Grouping**
===================================
        The `aggregate_and_group <aggregating.html>`_ method offers a flexible method for aggregating data, allowing users to:
        - Identify grouping columns.
        - Specify aggregation functions for each column: max, min, sum, mean, median, std, numique, first and last.        
        This class facilitates the creation of summarized datasets for more efficient analysis.

c. **Replace Excess Categories with "Other"**
=================================================
        The `replace_excess_values_with_other <excess_to_other.html>`_ method Address categorical data challenges by replacing less common values. Our application provides the option to:
        - Select columns for replacement.
        - Specify the number of top values to retain (default is 3).
        - Automatically replace excess categories with 'other' for improved data clarity.

d. **Feature Scaling**
===========================
        The `scale_features <feature_scaling.html>`_ method Standardizes or normalize numerical features for improved model performance. The application supports:
        - Scaling specific numerical features. If the list of specific features to scales is not provided, all numerical columns will be scaled.
        - Choosing between standardization and min-max scaling methods.  
        This ensures that numerical features contribute uniformly to the analysis.

e. **Merge Datasets**
============================
        The `merge_datasets <merge.html>`_ method Combines datasets seamlessly based on user-specified columns and merge type. Users can:        
        - Select datasets to merge.
        - Choose the merge type ('left', 'right', 'inner', 'outer').     
        This facilitates the integration of disparate datasets for a comprehensive analysis.
    These transformation capabilities enable users to mold their data to meet specific analytical requirements, enhancing the overall effectiveness of downstream analyses.

.. note::
  For examples of usage, refer to the `Google Colab Notebook <https://colab.research.google.com/drive/18l04pM7kgrD5VK-UNFJbG5mr0AL0we_o?usp=sharing>`_