# Predicting Life Insurance Claim Risk 

## Goal
  Predicts likelihood of Life insurance claims based on applicants demographics. 


## Key Insights:
- **Income, Credit Score, Health Score, and Claims History** are highly predictive of premium.
- **Log transformation** improved model accuracy significantl
- **XGBoost** slightly outperforms Linear Regression
    Both models are underfitting based on the negative R² score. A negative R² means the model performs worse than simply           predicting the mean of the target.

    However, XGBoost has:

   Lower MAE and MSE
    Slightly better R².yst.
- **Policy Age and Vehicle Age** are also strong premium indicates high correlations

  ###  Conclusion
This project successfully demonstrates how data-driven approaches can improve premium prediction accuracy for SecureLife Insurance Co.

Data preprocessing, such as handling missing values, encoding, and log transformation, significantly improved model stability.
XGBoost was the best performing model, though further tuning and more complex feature interactions could enhance results.
This work provides a solid foundation for building an intelligent insurance pricing system.
