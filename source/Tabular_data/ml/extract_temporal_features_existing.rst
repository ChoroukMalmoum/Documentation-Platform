extract_temporal_features_existing Function
===========================================

.. function:: extract_temporal_features_existing(data=None, timestamp_column='', timestamp_format='%Y-%m-%d %H:%M:%S')

    Extracts temporal features from a given time series dataset with an existing timestamp column. The function performs the following operations:

    1. **Timestamp Standardization**: 
       - Converts the timestamp data into a standardized format using the provided or inferred timestamp format. 
       - If the `timestamp_format` parameter is not specified, the function attempts to infer the format from the data.

    2. **Feature Extraction**: 
       - Computes and appends the following temporal features as new columns to the dataset:
         - Year: Extracts the year component from the timestamp.
         - Month: Extracts the month component from the timestamp.
         - Day: Extracts the day component from the timestamp.
         - Weekday: Extracts the weekday component, where Monday is denoted as 0 and Sunday as 6.
         - Hour: Extracts the hour component from the timestamp.
         - Minute: Extracts the minute component from the timestamp.
         - Second: Extracts the second component from the timestamp.
         - Date_Only: Constructs a date-only string representation (YYYY/MM/DD) from the timestamp.

    :param data: DataFrame, input time series dataset with a timestamp column.
    :param timestamp_column: str, name of the column containing timestamps.
    :param timestamp_format: str, format of the timestamp in the input data. Defaults to '%Y-%m-%d %H:%M:%S'.
    :return: DataFrame, the input data enriched with additional temporal features.
