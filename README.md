# TimeSeries-Fatigue-Detection

## Objective
This project classifies time-series accelerometer data from recreational runners to detect fatigue in running strides. The dataset includes strides labeled as **fatigued (F)** and **non-fatigued (NF)** for two subjects, A and B, recorded by an accelerometer sensor.

## Dataset
The dataset consists of time-series data for two subjects (A and B) stored in `fatigueA.csv` and `fatigueB.csv`. Each segment represents a stride and is labeled as either **F (fatigued)** or **NF (not fatigued)**. This subset is derived from a larger dataset.

## Approach
1. **Baseline Accuracy Calculation**:
   - Use a logistic regression model (`SGDClassifier`) on the raw time series data for subject A.
   
2. **Rocket Transformation for Time-Series Classification**:
   - Implement the **Rocket** (Random Convolutional Kernel Transform) transformer with an `SGDClassifier`, using the `sktime` toolkit, to classify subject A's strides.
   - **Evaluate Alternatives**:
     - Test alternative classifiers and normalisation methods to improve baseline accuracy on raw data.
     - Use different numbers of kernels with the Rocket transformer and assess alternative classifiers.
   
3. **Generalisation to Other Subjects**:
   - Apply the best-performing models from subject A to subject B, noting variations in accuracy and the impact of personalised vs. global modelling approaches.

## Requirements
This project requires:
- **sktime**: For the Rocket transformer implementation.
- **scikit-learn**: For the SGDClassifier and other classifiers.
- **pandas**: For data handling.
- **matplotlib**: For visualising results, such as accuracy trends and confusion matrices.

## Getting Started
1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/Time-Series-Fatigue-Detection.git
   ```
2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```
3. Open and run `RunningCore.ipynb` to follow the project and see results.

## Results
The project reports on:
- Baseline accuracy using logistic regression.
- Improved accuracy with Rocket transformations, alternative classifiers, and optimal kernel numbers.
- Model generalisability from subject A to subject B, with a focus on personalised vs. global model performance.

## Contributing
Contributions are welcome! For major changes, please open an issue to discuss proposed updates.

---

### Additional Files
- **requirements.txt**: List all dependencies (`sktime`, `scikit-learn`, `pandas`, `matplotlib`).
- **LICENSE**: Add a license file, such as MIT, if needed.
- **RunningCore.ipynb**: Main Jupyter Notebook containing the code, markdown analysis, and visualisations.


---
