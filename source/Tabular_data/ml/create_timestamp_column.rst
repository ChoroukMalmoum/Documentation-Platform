create_timestamp_column Function
=================================

.. function:: create_timestamp_column(data, year_col, month_col, day_col, hour_col=None, minute_col=None, second_col=None)

    Synthesizes a unified timestamp column in a time series dataset from user-specified temporal columns. The function performs the following operations:

    1. **Column Combination**: Merges user-provided columns for Year, Month, Day, Hour, Minute, and Second to construct a unified timestamp column.
    
    2. **Timestamp Generation**: Creates a new timestamp column using the combined temporal columns, producing a consolidated temporal reference for each data entry in the dataset.

    :param data: DataFrame, input time series dataset.
    :param year_col: str, name of the column containing the year information.
    :param month_col: str, name of the column containing the month information.
    :param day_col: str, name of the column containing the day information.
    :param hour_col: str, optional, name of the column containing the hour information. Defaults to None.
    :param minute_col: str, optional, name of the column containing the minute information. Defaults to None.
    :param second_col: str, optional, name of the column containing the second information. Defaults to None.
    :return: DataFrame, the input data with a newly created timestamp column.
