# Final_Python_Assignment

This is a pipeline for dataset building from raw data in separated folders (each folders is specific for a subject). Also, this pipeline it can be used for preprocessing of the data
(outlier detection, graphical overview with differents type of plot), assumption check of Linear Mixed Effect Models on python and lmer formula for analyzing a specifc conditions.
This is a replication of another pipeline that I wrote on MATLAB and R for doing about the same things - and it was useful for checking the consistency of the results.

For instance, generating again from zero the dataset on Python it was important for checking the original dataset generated with MATLAB from the raw data - in order to see 
if the data are the same. Also the graphs generateted with Python (matplotlib and seaborn) were important for checking the consistency and reliability of the 
ohter graphs generated with R and ggplot.

However the data analysis of the main project on MATLAB and R are not completed, so the idea was replicating those analysis already done (preprocessing, assumption, outlier) 
for checking the consistency with another language program.


The script is organized in this way:

1) First part dedicated to recollect data from the single-subject folders and store it in a long-format table suitable for the analysis. 

2) Second part dedicated to preprocessing and data plotting for visual inspection.

3) lmer analysis with statsmodel package and assumption check.

___________

Areas to improve in the future:

1) Some warnings are present in the script, primarily due to the fact that some line of code that I used will be deprecated in the future in the new library version (for intance seaborn)

2) Statsmodel does not support at 100% the lmer model. R in this case is more suitable with dedicated package as lme4 and emmeans. Indeed, statsmodel supports a different type of
	formula to use for the lmer analysis compared to R (random slope and random intercept are expressed in a different manner and this can be problematic for the replication
	of the results). Moreover, statsmodel seems not to support the pairwise comparison after the application of the lmer formula. 
	There is a package called pymer4 that runs R from Python that partially solve this issues, but I was not able to install it (intsallation would continuously freeze or crash on 
	anaconda). See this for the differences between statsmoodel, pymer4 and lme4 --> https://towardsdatascience.com/how-to-run-linear-mixed-effects-models-in-python-jupyter-notebooks-4f8079c4b589
	and --> https://www.statsmodels.org/dev/examples/notebooks/generated/mixed_lm_example.html

