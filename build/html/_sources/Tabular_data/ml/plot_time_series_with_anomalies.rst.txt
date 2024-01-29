plot_time_series_with_anomalies Function
=========================================

.. function:: plot_time_series_with_anomalies(df, x_col, y_col, anomaly_col)

    Visualizes a time series dataset along with its detected anomalies. The function performs the following operations:

    1. **Time Series Plotting**: Plots the main time series data using the provided x-axis (`x_col`) and y-axis (`y_col`) columns.
    
    2. **Anomaly Highlighting**: Superimposes the anomalies onto the time series plot, marking them with a distinctive color (typically red).

    :param df: DataFrame, input time series dataset.
    :param x_col: str, column name for the x-axis values (e.g., timestamps or indices).
    :param y_col: str, column name for the y-axis values (e.g., measurements or values).
    :param anomaly_col: str, column name indicating anomalies in the dataset (usually binary: 1 for anomaly, 0 for normal).
    :return: Plot, a visualization showing the time series data with highlighted anomalies.
