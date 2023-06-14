## Project report

    We have data from Yandex.Realty classified https://realty.yandex.ru containing real estate listings
    for apartments in St. Petersburg and Leningrad Oblast from 2016 till the middle of August 2018. 
    In this Lab you'll learn how to apply machine learning algorithms to solve business problems. 
    Accurate price prediction can help to find fraudsters automatically and help Yandex.Realty users 
    to make better decisions when buying and selling real estate.
    
    
  ## Data description
  
    The data I've used for prediction model includes such features as open_plan, rooms,  area,  renovation.
    
    The preproccessing includes spliting dataset to train and validation datasets and cleaning the data with NaN values.
    Pipeline includes standartization by StandardScaler.
    
   ## Model description
  
    I have tried the following models:
    "  
    "    DecisionTreeRegressor
    "    LinearRegression
    "    RandomForestRegressor
    "    CatBoostRegressor
    "    LGBMRegressor
    "    ElasticNet.
    "   
    After comparison the mean prediction errors, the best model proved to be the LGBMRegressor.
    I have trained this model using the following Hyperparameters, tested in the following ranges:
  
        num_leaves: [3, 20]
        reg_alpha: [0.1, 0.5]
        min_data_in_leaf: [30, 50, 100, 300]
        lambda_l1: [0, 1, 1.5]
        lambda_l2: [0, 1]
