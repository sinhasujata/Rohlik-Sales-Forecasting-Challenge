# Rohlik-Sales-Forecasting-Challenge - Enhancing Model Performance with Lagged Features in XGBoost

## Key Highlights:

1. **Data Exploration:** Understanding the dataset by analyzing historical sales trends, missing values, and data distributions to prepare it for feature engineering.
2. **Lagged Features:** Creating historical feature representations to capture temporal dependencies in sales data. These features reveal trends and seasonality crucial for accurate time-series forecasting.
3. **Feature Engineering & Selection:** Identifying and selecting relevant features, scaling numerical values, encoding categorical variables, and testing feature importance to refine the dataset for optimal model performance.
4. **Model Training with XGBoost:** Leveraging XGBoost’s gradient boosting capabilities to build an effective sales prediction model.
5. **Validation & Performance Analysis:** Evaluating the model’s accuracy using metrics like RMSE and WMAE. Cross-validation is applied to ensure the model generalizes well to unseen data.
6. **Model Optimization & Deployment:** Strategies for improving model efficiency, reducing overfitting, and integrating the model into a production pipeline for real-world business applications.

## Approach & Model Improvements

- **Initial Feature Engineering:** Started with the given dataset, handling null values and categorizing features as numerical and categorical. This initial setup yielded a public score of approximately **47**. 
- **Incorporating Lag Features & Seasonal Cyclic Trends:** Introduced lagged sales values and cyclic seasonal sales features, which significantly improved the model and reduced the public score to **30**. 
- **Loss Function Optimization with Weights:** Integrated the provided weights into the Weighted Mean Absolute Error (WMAE) loss function, further reducing the score to **27**. 
- **Experimenting with Discounts & Sales Impact:** Analyzed the effect of discounts, maximum discounts, store closures, and holidays on sales, though these modifications had minimal impact on the overall performance.
- **Normalization & Transformation:** Applied log normalization to sell_price_main and min-max normalization to total_orders (as some values were zero). Additionally, transformed the names column by extracting common names from identifiers, leading to a final score improvement to around **25**.

I have attached the public and private scores at the end.

## Attribution & Copyright Notice:

This project is inspired by the Rohlik Sales Forecasting Challenge V2 on Kaggle. The dataset and competition details are provided by Rohlik Group and Kaggle under their respective terms of use. Any results, analysis, and insights presented in this blog post are for educational and informational purposes only. Please refer to the original [Kaggle competition page](https://www.kaggle.com/competitions/rohlik-sales-forecasting-challenge-v2/overview) for official details and dataset access. All credits for the dataset and competition organization belong to Rohlik Group and Kaggle.
