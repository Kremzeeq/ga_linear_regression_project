# Web Traffic Data Exploration
## with Linear Regression Analysis


![google_search](/assets/google_search_pic.jpg "google_search_pic")

## Overview

This Web Traffic Data Exploration Project involves a deepdive in some Google Analytics data, available here:

[assets/GA_web_traffic_data_12_08_20.csv](https://github.com/Kremzeeq/ga_linear_regression_project/blob/master/assets/GA_web_traffic_data_12_08_20.csv)

There are four parts to the project, and these are viewable as webpages, via links below:

1. [Introduction to data set](https://htmlpreview.github.io/?https://github.com/Kremzeeq/ga_linear_regression_project/blob/master/webpages/GA_Linear_Regression_Analysis_P1.html)
2. [Preparation for Running Linear Regression Analysis](https://htmlpreview.github.io/?https://github.com/Kremzeeq/ga_linear_regression_project/blob/master/webpages/GA_Linear_Regression_Analysis_P2.html)
3. [Running Linear Regression with sklearn](https://htmlpreview.github.io/?https://github.com/Kremzeeq/ga_linear_regression_project/blob/master/webpages/GA_Linear_Regression_Analysis_P3.html)
4. [Web Traffic Dashboard on Kaggle](https://www.kaggle.com/kremzeeq/ga-linear-regression-analysis-dashboarding/edit)

**Parts 1-3** can be followed like a tutorial with Jupyter notebook. If you choose to do so, it is recommended to install modules listed within [requirements.txt](https://github.com/Kremzeeq/ga_linear_regression_project/blob/master/requirements.txt). The python version configured with this was 3.7.5.

[Part 3](https://htmlpreview.github.io/?https://github.com/Kremzeeq/ga_linear_regression_project/blob/master/webpages/GA_Linear_Regression_Analysis_P3.html) provides steps for accessing the notebook online via Kaggle. However if you have Anaconda installed...

**Running the dashboard locally seems preferable**

Here's the [jupyter notebook](https://github.com/Kremzeeq/ga_linear_regression_project/blob/master/jupyter_notebooks/GA_Linear_Regression_Analysis_P4-Dashboarding.ipynb) with source code for reproducing the dashboard. 

This has been produced using a Virtual Environment with Python 3.7.5.

Please ensure to install the requirements for the project. This command helps ensure all requirements are installed

```
while read requirement; do conda install --yes $requirement; done < requirements.txt
```

## Known issues with dashboard

* **Section A**: 
* If you enter a number of Users to predict Page Views or Sessions, the output stacks and does not refresh with each click of the submit button. Functionality associated with clicking the button should also handle ValueErrors. 

* **Section B**: 
* This currently considers all months within the Google Analytics data file. However, if alternative data is used, there is a possibly that the latest month would be incomplete, in which case, 3-month moving averages wouldn't look right. This means the previous complete month should be considered as the latest month instead. 
* When you select an option from the dropdown menus in the Kaggle notebook, the transitionary flash is distracting for the end-user and the report scrolls up slightly, so section B is no longer in focus.

## Other issues

* This report accepts Avg. Session Duration in seconds. Please note, if you use alternative web traffic data, Avg. Session Duration may be provided in HH:MM:SS which would prompt errors in the Jupyter notebook for producing the dashboard. Therefore, code could be adapted to handle this error.

* The more cells in the jupypter notebook for the dashboard, the more white space! Thus you need to scroll down a little to view Section B.



## Notes on the Jupyter Notebook dashboard:

* The web traffic data file has a different path in the Kaggle notebook: '../input/ga-web-traffic-data-12-08-20/GA_web_traffic_data_12_08_20.csv'

* There is a cell which contains the following in a cell in the Jupyter notebook that hides code once all cells are run. To view code again, you need to convert this to Markdown:

%%html
<style>
div.input {
    display:none;
}
.widgetTitle {
    font-style: bold;
    font-size: 16px;
}

.yMetricSelector {
    float: right
}

</style>






