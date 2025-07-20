# How to Run the Cyclone Preheater Anomaly Detection Project

## Prerequisites

- Python 3.8 or higher
- Jupyter Notebook or JupyterLab
- The Data.csv file containing the cyclone preheater data

## Step 1: Install Required Libraries

1. Create a new file named `requirements.txt` with the following content:
```
numpy==1.24.3
pandas==2.0.2
matplotlib==3.7.1
seaborn==0.12.2
scikit-learn==1.2.2
scipy==1.10.1
```

2. Open a command prompt or terminal and install the requirements:
```bash
pip install -r requirements.txt
```

## Step 2: Set Up Project Structure

1. Create a new project folder named `cyclone-anomaly-detection`
2. Inside this folder, create two subdirectories:
   - `visualisations`
   - `results`
3. Place the `Data.csv` file in the main project folder
4. Place the `main.ipynb` notebook file in the main project folder

Your folder structure should look like this:
```
cyclone-anomaly-detection/
├── requirements.txt
├── main.ipynb
├── Data.csv
├── visualisations/
└── results/
```

## Step 3: Run the Analysis

1. Start Jupyter Notebook:
```bash
jupyter notebook
```

2. Navigate to your project folder and open `main.ipynb`

3. Run each cell in sequence by clicking the "Run" button or using Shift+Enter

4. The notebook will perform the following operations:
   - Load and preprocess the data
   - Scale the features using Min-Max scaling
   - Optimize DBSCAN parameters 
   - Detect anomalies
   - Generate visualizations saved to the `visualisations` folder
   - Save anomaly detection results to the `results` folder

5. All visualizations will be automatically saved to the respective folders as the notebook runs

## Note on Memory Usage

The dataset contains approximately 377,719 records, which may require significant memory. If you encounter memory issues:

- Try closing other applications
- If using Windows, ensure your virtual memory is adequately configured
- For MacOS/Linux, consider increasing your swap space

## Viewing the Results

After running the notebook:

1. The preprocessed data will be saved as `processed_data.csv`
2. The scaled data will be saved as `scaled_data.csv`
3. Visualizations will be available in the `visualisations` folder
4. Anomaly detection results will be in the `results` folder, including:
   - `anomaly_detection_results.csv` - Complete dataset with anomaly labels
   - `anomaly_periods.txt` - List of continuous time periods with anomalies
   - Various plots showing anomalies for each variable

## Troubleshooting

- If visualizations don't appear in the notebook, check if matplotlib is properly configured
- If DBSCAN parameter optimization takes too long, you can use the pre-optimized values mentioned in the notebook
