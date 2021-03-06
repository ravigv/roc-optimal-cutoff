# Determining Optimal Probability Cutoffs with ROC Curve
## Installation
Open terminal in this directory and run either:
1. pip install the module itself
```
pip install .
```
2. setup.py (same as 1)
```
python setup.py install
```
3. setup.py with testing
```
chmod a+x setup.sh
./setup.sh
```
4. docker-compose to set up an environment with module installed
```
docker-compose up -d
```
## Getting Started
```
import thresholder

proba_thresholder = thresholder.ROC_Thresholder()
proba_thresholder.fit(predict_proba, true_Y, "./ROC_output/") # determine optimal thresholds and save plots
roc_preds = proba_thresholder.transform(predict_proba) # obtain predictions based on optimal cutoffs
```

## Jupyter Notebook Server
To set up a notebook server, follow step 4 of **Installation** and assuming default settings are applied, head to *http://localhost:8889/tree* to view existing or create new notebooks to perform experiments with the module.

## Testing Your Alterations
```
chmod a+x test.sh
./test.sh
```