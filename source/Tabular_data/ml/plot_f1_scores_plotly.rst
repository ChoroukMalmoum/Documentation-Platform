plot_f1_scores_plotly Function
===============================

.. function:: plot_f1_scores_plotly(f1_scores_dict)

    Generates a Plotly bar chart to visualize the F1 scores of various anomaly detection methods. The function performs the following operations:

    1. **Data Preparation**: Extracts the model names and corresponding F1 scores from the provided dictionary.
    
    2. **Visualization**: Constructs a bar chart using Plotly, where each bar represents the F1 score of a specific anomaly detection method.

    :param f1_scores_dict: dict, a dictionary containing the F1 scores for different anomaly detection methods.
    :return: Plot, a visual representation of the F1 scores using a bar chart in Plotly.
