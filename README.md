<div align="center">
  <img src="imgs/logo-light-nobg.png" alt="logo" width="128"/>
  <h1>Sales forecasting</h1>

</div>

<div align="justify">

This project focuses on sales prediction and data enrichment using the Catboost algorithm and Upgini. The goal is to forecast future sales for the next 3 months and determine whether enriching the data leads to an increase in model accuracy.

## Roadmap

- [x] Perform basic exploratory data analysis to gain insights into the sales data
- [x] Apply the Catboost algorithm for time series forecasting, considering relevant features identified during EDA
- [x] Enhance the dataset using Upgini to assign higher weights to uncertain and informative data points
- [x] Use the enriched dataset to retrain the Catboost model and generate more accurate sales forecasts
- [x] Assess the model's performance using the Symmetric Mean Absolute Percentage Error (SMAPE) metric
- [x] Compare the SMAPE values before and after data enrichment to evaluate the impact of Upgini
- [x] Summarize the findings and highlight the effectiveness of Upgini in improving the accuracy of the Catboost model


## Stack

- EDA
- Catboost
- Upgini

## Data Overview

- Tabular data
- 5 years' worth of product sales
- 4 features:
  - date, store_id, item_id, and sales
- Sales data before 2017 will be used as training data, while everything older than 2017 will be our test data
- limited information (i.e., only date and sales are useful) for our model to understand how to successfully predict future sales

## Methodology

The methodology consists of three key steps: basic exploratory data analysis, application of the Catboost algorithm, and data enrichment using Upgini.

### Exploratory Data Analysis (EDA):

The initial step involves conducting some really basic exploratory data analysis to gain insights into the sales data.

### Model creation using the Catboost algorithm:

Once the data has been briefly analyzed, the Catboost algorithm will be applied to build a time series forecasting model. Catboost is a gradient-boosting algorithm that handles categorical features effectively and has shown promising performance in various domains. The model will then be trained on our sales data, considering relevant features identified during the exploratory data analysis.

### Data Enrichment with Upgini:

To further enhance the forecasting model, the data will be enriched using Upgini. The latter is a data enrichment method that enhances the importance of uncertain and informative data points during the training process. By assigning higher weights to such data instances, the model can effectively capture the nuances and dependencies within the data, leading to improved predictions. The enriched dataset will be used to retrain the Catboost model, leveraging the enhanced representation of the data to generate more accurate sales forecasts.

### Symmetric Mean Absolute Percentage Error (SMAPE)

The evaluation of the developed model will primarily be based on the SMAPE metric, which measures the accuracy of the predictions compared to the actual sales values. The performance of the model will be assessed by comparing the SMAPE values before and after data enrichment using Upgini.


## Evaluation and Conclusion

To assess whether our enrichment process led to significant results, we employed the Symmetric Mean Absolute Percentage Error (SMAPE) metric, which measures the accuracy of our predictions compared to the actual values. Initially, our baseline model yielded a SMAPE value of 37%.

However, by employing Upgini, we were able to prioritize uncertain and informative data points during training. This technique played a crucial role in identifying and assigning higher weights to data instances that were previously underrepresented, leading to a more accurate prediction model and a lower SMAPE value of 14%.

Overall, by incorporating Upgini to enrich our data and retraining the CatBoostRegressor model, we successfully achieved a significant reduction in the SMAPE value. This outcome underscores the effectiveness of Upgini in enhancing the model's accuracy and reaffirms the value of CatBoostRegressor as a robust algorithm for regression tasks.

## License

[MIT](https://github.com/1391819/sales-forecasting/blob/main/License.txt) © [Roberto Nacu](https://github.com/1391819)
