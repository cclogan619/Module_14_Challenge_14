# Module 14 Challenge
Module 14 challenge repository containing machine learning models that enhance the existing trading signals of a financial advisory firm with machine learning algorithms that can adapt to new data.

## Results

First, a baseline SVC model was developed, trained and compared against actual returns. It had an accuracy score of 0.55 and provided the following cumulative returns compared to the actual returns:
![BaselinePerformance](/Images/BaselinePerformance.png)

Then the model was tuned two different ways:
1. The size of the training dataset was increased from 3 months to 9 months. This resulted in a slightly lower accuracy score of 0.53 and worse cumulative returns than the baseline:
![AdjustedTrainingSizePerformance](/Images/AdjustedTrainingSizePerformance.png)
2. The SMA input features were adjusted (short SMA: 4->10, long SMA: 100->200). This resulted in the same accuracy score but worse cumulative returns than the baseline:
![AdjustedSMAPerformance](/Images/AdjustedSMAPerformance.png)

To further test the baseline performance, a new DecisionTree model was created and compared with the baseline performance. However, this new model resulted in significantly lower accuracy (0.45) and worse returns as seen here:
![AlternateModelPerformance](/Images/AlternateModelPerformance.png)

In conclusion, the baseline SVC model ended up being the best model and is the one that is recommended to the firm.

## Technologies

This project leverages Python 3.7 in Jupyter Lab with the following packages:

* [pandas](https://pandas.pydata.org/) - For financial data analysis tools
* [numpy](https://numpy.org/) - For numerical functions to aid in financial calculations
* [scikit-learn](https://scikit-learn.org/stable/user_guide.html) - To create models for fitting data and making predictions

## Contributors

Starter code for this app was provided by the GWU Fintech Bootcamp program. Updates to that code to fulfill the analysis were done by Peter Lefebvre (peter.c.lefebvre@gmail.com).

## License

[MIT License](https://github.com/plefebvre1/module_14_challenge/blob/main/LICENSE)
