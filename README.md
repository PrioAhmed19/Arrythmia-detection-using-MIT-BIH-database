# Arrhythmia Detection using MIT-BIH Database

## Project Overview

This repository contains a machine learning project focused on the detection of cardiac arrhythmias using electrocardiographic (ECG) signals from the MIT-BIH Arrhythmia Database. The project explores and compares the performance of various neural network architectures, specifically Convolutional Neural Networks (CNN), Dense Neural Networks (DNN), and Long Short-Term Memory (LSTM) networks, in accurately identifying arrhythmias from graphical representations of ECG data.

## Research Objective

The primary objective of this research is to evaluate and compare the accuracy of different neural network models (CNN, DNN, and LSTM) in detecting arrhythmias. The project aims to predict heartbeats from ECG signals, specifically focusing on the first ECG peak of each heartbeat. The approach simplifies the problem by assuming the presence of a QRS detector capable of automatically identifying heartbeat peaks, and utilizes a windowed approach for analysis, comparing current heartbeats to preceding and succeeding ones.

## Data Description

The dataset used in this project is the MIT-BIH Arrhythmia Database, a widely recognized standard for evaluating arrhythmia detectors. It comprises 48 half-hour, two-channel ambulatory ECG recordings collected from 47 subjects between 1975 and 1979 by the BIH Arrhythmia Laboratory. 

Key characteristics of the dataset:
- **Recordings:** 48 half-hour ambulatory ECG recordings.
- **Channels:** Two-channel ECG signals.
- **Subjects:** Data from 47 individuals.
- **Annotation:** Each heartbeat (approximately 110,000 annotations in total) is independently annotated by two or more cardiologists, with disagreements resolved to ensure accuracy.
- **Sampling Rate:** Signals are digitized at 360 samples per second with 11-bit resolution.

For more details on the dataset, please refer to the [Kaggle dataset page](https://www.kaggle.com/datasets/klmsathishkumar/mit-bih-arrhythmia-database?resource=download).

## Project Structure

- `arrhythmia prediction.ipynb`: This Jupyter Notebook contains the core code for data loading, preprocessing, model definition (CNN, DNN, LSTM), training, and evaluation. It includes detailed steps for:
    - Importing necessary libraries.
    - Data transformation and analysis.
    - Data preprocessing techniques.
    - Training various neural network models.
    - Evaluating model performance using relevant metrics.

## Installation and Usage

To run this project, you will need to have Python installed along with several libraries. It is recommended to use a virtual environment.

1.  **Clone the repository:**
    ```bash
    git clone https://github.com/PrioAhmed19/Arrythmia-detection-using-MIT-BIH-database.git
    cd Arrythmia-detection-using-MIT-BIH-database
    ```

2.  **Create a virtual environment (optional but recommended):**
    ```bash
    python -m venv venv
    source venv/bin/activate  # On Windows, use `venv\Scripts\activate`
    ```

3.  **Install the required packages:**
    The necessary packages are typically listed in a `requirements.txt` file. Since one is not provided, you will likely need the following:
    ```bash
    pip install numpy pandas matplotlib scikit-learn tensorflow keras
    ```
    *Note: The specific versions of these libraries might be important for reproducibility. Please refer to the notebook for exact versions if you encounter issues.*

4.  **Download the dataset:**
    The MIT-BIH Arrhythmia Database needs to be downloaded separately. You can find it on [Kaggle](https://www.kaggle.com/datasets/klmsathishkumar/mit-bih-arrhythmia-database?resource=download). Follow the instructions on Kaggle to download the dataset and place it in a suitable directory, or modify the notebook to point to your data location.

5.  **Run the Jupyter Notebook:**
    ```bash
    jupyter notebook "arrhythmia prediction.ipynb"
    ```
    This will open the notebook in your web browser, where you can execute the cells sequentially to reproduce the analysis and model training.

## Models and Evaluation

The project compares three types of neural networks:

-   **Convolutional Neural Networks (CNN):** Effective for capturing spatial hierarchies in data, suitable for analyzing patterns in ECG signals.
-   **Dense Neural Networks (DNN):** Fully connected layers for general pattern recognition.
-   **Long Short-Term Memory (LSTM):** Recurrent neural networks particularly well-suited for sequential data like time-series ECG signals.

The notebook includes sections for:
-   **Importing Packages:** Essential libraries for data manipulation, visualization, and model building.
-   **Data Transformation:** Steps to prepare the raw ECG data for model input.
-   **Analyzing Data:** Exploratory data analysis to understand the characteristics of the ECG signals and annotations.
-   **Data Preprocessing:** Techniques such as normalization, segmentation, and windowing applied to the ECG data.
-   **Training Models:** Implementation and training procedures for CNN, DNN, and LSTM models.
-   **Evaluation Metrics:** Metrics used to assess the performance of each model, such as accuracy, precision, recall, F1-score, and ROC curves.

## Future Enhancements

-   Explore more advanced deep learning architectures.
-   Integrate real-time ECG data processing capabilities.
-   Develop a user-friendly interface for arrhythmia detection.
-   Expand the dataset to include more diverse arrhythmia types.


## Contributing

Contributions are welcome! Please feel free to fork the repository, create a new branch, and submit pull requests. For major changes, please open an issue first to discuss what you would like to change.

## Contact

For any questions or inquiries, please contact [PrioAhmed19](https://github.com/PrioAhmed19).


