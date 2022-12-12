# MLE Bias Correction

Loosely following the procedure in:

Pragya Sur and Emmanuel J. Candès. A modern maximum-likelihood theory for high-
dimensional logistic regression. Proceedings of the National Academy of Sciences, 116
(29):14516–14525, July 2019. ISSN 0027-8424, 1091-6490. doi: 10.1073/pnas.1810420116.
URL https://pnas.org/doi/full/10.1073/pnas.1810420116.

However, we do not attempt to solve the system of equations or estimate the signal strength from the sample directly. This is replaced with a double-sampling method where we make population inferences from the dataset and draw low EPV samples. We attempt to apply our de-biased coefficients, comparing the predictive power of MLE models trained on the population and sample against the bias-corrected samples. This is largely unsuccessful when we apply it to real-world data in the auto-mpg dataset, but does okay with simulated data.

# Files

1. Cars_Data is the auto-mpg dataset, taken from https://data.world/dataman-udit/cars-data
2. cars-intercept.ipynb is the notebook in which we fit logistic regression models with intercept terms to the auto-mpg dataset.
3. Generated.ipynb is a bunch of noodling around and then a reasonably successful application of the same methodology used in cars-intercept to well-behaved simulated data.
