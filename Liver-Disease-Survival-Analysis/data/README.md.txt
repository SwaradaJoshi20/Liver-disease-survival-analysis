# Dataset Information

## Source
This project uses the **Primary Biliary Cholangitis (PBC) Dataset** from the Mayo Clinic.

## How to Obtain the Data
The dataset is publicly available and can be loaded directly in R or Python:

### In R (Easiest method):
```r
library(survival)
data(pbc)

### In Python (using the lifelines library):
from lifelines.datasets import load_pbc
pbc_df = load_pbc()

### Download from Kaggle:
Search for "Mayo Clinic Primary Biliary Cirrhosis (PBC) Data" on Kaggle Datasets.

### Note:
The raw data file is not included in this repository. Please use the methods above to acquire the data to run the code in this repository.