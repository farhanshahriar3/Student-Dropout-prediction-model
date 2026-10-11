# Dataset Notes

`student_dropout_cleaned.csv` is the cleaned dataset used by the notebook. It contains 4,424 records and 37 columns, with `target` as the outcome column.

The target values are `Dropout`, `Enrolled`, and `Graduate`. The notebook removes `Enrolled` before training so that model evaluation compares only `Dropout` and `Graduate`.

The feature names and values are retained in the supplied CSV. Any external redistribution or reuse should follow the terms of the original dataset source and applicable privacy requirements.
