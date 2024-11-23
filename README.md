# Task Description
Analyze provided data files, preprocess as necessary, and perform model fitting to compare results.

## File Descriptions

### Data Files
- **YYYYMMDD.xy**: Each file contains a day's worth of data, with the filename corresponding to the date (e.g., 20220425.xy).

### Supporting Files
1. **xy_parser.py**: Contains methods to parse `.xy` files and convert the data into a Pandas DataFrame.
2. **demo.py**: Demonstrates how to use `xy_parser.py`.
3. **baseline_model.json**: Provides a reference linear model for comparison, including:
   - **Coefficients**: Feature coefficients.
   - **Constant**: Intercept.
   - **InputNames**: Feature names (corresponding to column names in `.xy` files).

### `.xy` Data Format
- Columns:
  - `Timestamp`: Time information.
  - `X0` to `X149`: Features.
  - `Y`: Target variable (to be predicted).

### File Structure
```
├── baseline_model.json
├── demo.py
├── xy_parser.py
├── xy_train/ [Training data]
│   ├── 20220425.xy
│   ├── 20220426.xy
│   ├── ...
└── xy_validate/ [Validation data]
    ├── 20220701.xy
    ├── ...
```

---

# Tasks

1. **Feature Analysis**: 
   - Analyze features from `.xy` files to determine whether preprocessing or cleaning is required.
2. **Target Variable Analysis**: 
   - Examine the characteristics of the target variable, `Y`.
3. **Feature-Target Relationship**:
   - Investigate the relationships between features and `Y`.
4. **Linear Model Fitting**:
   - Train 1-2 linear models on training data (`20220425-20220630`), validate on unseen data (`202207`), and compare with actual `Y` values.
5. **Nonlinear Model Fitting**:
   - Train 1-2 nonlinear models using the same training and validation sets, and compare predictions with actual `Y`.
6. **Model Comparison**:
   - Compare models (linear, nonlinear, and baseline) for in-sample and out-of-sample performance.
7. **Summary**:
   - Summarize findings from the above steps.
