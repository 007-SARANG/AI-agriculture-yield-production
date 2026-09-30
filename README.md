# 🌾 AI in Agriculture: Crop Monitoring and Yield Prediction

## 📄 Project Overview

This project leverages machine learning techniques to predict **Rice Yield (Kg/ha)** using year, cultivation area, and state as candidate input features. It demonstrates the use of **EDA**, **outlier removal**, **data preprocessing**, **model training**, and **evaluation**.

---

## 📊 Dataset

### Source:

- `Crops_data.csv` (original raw data)

### Derived Datasets:

- `rice_data.csv`: Extracted rice-related data
- `rice_data_outlier_removed.csv`: Cleaned rice dataset after removing outliers using IQR

---

## 📚 Notebooks

| Notebook                         | Description                                                                                           |
| -------------------------------- | ----------------------------------------------------------------------------------------------------- |
| `01_Preprocessing.ipynb`         | Loaded original dataset, filtered for rice, handled missing/null values, encoded categorical features |
| `02_EDA.ipynb`                   | Performed data visualization, outlier detection and removal (IQR method), and saved the cleaned data  |
| `03_Modelling.ipynb`             | Trained Random Forest model, performed scaling, trained/test split, saved model and scaler            |
| `04_Evaluation_Deployment.ipynb` | Evaluated the model (R², MAE, RMSE), plotted results, and saved prediction output                     |

---

## Evaluation status

The README previously reported a 99.2% training score and a 95.4% test R². Those figures are withdrawn: the original model feature set included total production, which directly encodes yield together with area, and the outlier filtering was performed before the train/test split. The saved model and historical scores should not be treated as valid generalization results. The modeling notebook now excludes total production and uses repository-relative paths; rerun the preprocessing and evaluation with a split-first methodology before publishing replacement metrics.

---

## 🔧 Tech Stack

- **Language**: Python
- **Libraries**: pandas, numpy, matplotlib, seaborn, sklearn
- **IDE**: Jupyter Notebook (Anaconda)

---

## 📢 Notes

- Outliers were removed using IQR before training.
- Data was scaled using `StandardScaler`.
- Cross-validation was also explored to prevent overfitting.

---

## 🚀 How to Run

1. Clone the repository
2. Install dependencies: `pip install -r Requirements.txt`
3. Run notebooks in sequence: `01` to `04`
4. Rerun the preprocessing, training, and evaluation notebooks to create the model artifacts.

---

## Attribution

This repository is a collaborative fork of [nupurmadaan04/AI-agriculture-yield-production](https://github.com/nupurmadaan04/AI-agriculture-yield-production). The upstream README credits Nupur Madaan and identifies this as an internship project.

---

## 📅 License

This project is licensed under the [MIT License](LICENSE).


