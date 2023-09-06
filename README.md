# Final_Python_Assignment

This is a pipeline for building datasets from raw data stored in separate folders, with each folder specific to a subject. Additionally, this pipeline can be used for data preprocessing, which includes outlier detection, creating graphical overviews with different types of plots, and checking assumptions for Linear Mixed Effect Models in Python. It also involves using an 'lmer' formula for analyzing specific conditions. This pipeline is a replication of another one I previously created in MATLAB and R, which served the same purpose and was useful for ensuring the consistency of the results.

For example, recreating the dataset from scratch in Python was crucial for verifying the original dataset generated in MATLAB from the raw data, ensuring data consistency. The graphs generated with Python using libraries like Matplotlib and Seaborn were also essential for confirming the consistency and reliability of other graphs generated with R and ggplot.

However, the data analysis for the primary project in MATLAB and R is not yet complete. The idea here is to replicate the analyses already performed (preprocessing, assumption checking, and outlier detection) to ensure consistency across different programming languages.

The script is organized as follows:

The first part is dedicated to collecting data from the individual subject folders and storing it in a long-format table suitable for analysis.

The second part focuses on preprocessing and generating data plots for visual inspection.

Finally, it involves running an lmer analysis using the Statsmodels package and checking assumptions.

In the repository, you'll find two CSV files as examples of dataset creation from raw data. One file contains single trial data for each subject, while the other combines data across conditions and averages them.

Please note that you need to adjust the directory paths in the code to match where your data is stored or where you want to save the results in order to make the script run successfully.

Areas for future improvement:

There are some warnings present in the script, primarily because certain lines of code may be deprecated in future library versions, such as Seaborn.

Statsmodels does not fully support the 'lmer' model. In this case, R is more suitable, as it offers dedicated packages like 'lme4' and 'emmeans.' Notably, Statsmodels uses a different formula syntax for 'lmer' analysis compared to R, which can be challenging when replicating results. Additionally, Statsmodels appears not to support pairwise comparisons after applying the 'lmer' formula. There is a package called 'pymer4' that runs R from Python, partially addressing these issues. However, I encountered difficulties installing 'pymer4' as it would often freeze or crash in Anaconda. For more information on the differences between Statsmodels, pymer4, and lme4, refer to these resources: [Link 1](https://www.statsmodels.org/dev/examples/notebooks/generated/mixed_lm_example.html) [Link
](https://towardsdatascience.com/how-to-run-linear-mixed-effects-models-in-python-jupyter-notebooks-4f8079c4b589)
