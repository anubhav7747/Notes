# Machine Learning Pipeline
A Machine Learning pipeline is a process of automating the workflow of a complete machine learning task. It can be done by enabling a sequence of data to be transformed and correlated together in a model that can be analyzed to get the output. A typical pipeline includes raw data input, features, outputs, model parameters, ML models, and Predictions. It means that in the pipeline, each step is designed as an independent module, and all these modules are tied together to get the final result.

## Importance of Machine Learning Pipeline
![machine-learning-pipeline2](https://github.com/anubhav7747/Notes/assets/77168708/678eb184-b62e-40e3-ba59-b0e0aafa3a66)

A typical workflow consists of Ingestion, Data cleaning, Data pre-processing, Modelling, and deployment.

In ML workflow, all these steps are run together with the same script. It means the same script will be used to extract data, clean data, model, and deploy. However, it may generate issues while trying to scale an ML model. These issues involve:
- If we need to deploy multiple versions of the same model, we need to run the complete workflow cycle multiple times, even when the very first step, i.e., ingestion and preparation, are exactly similar in each model.
- If we want to expand our model, we need to copy and paste the code from the beginning of the process, which is an inefficient and bad way of software development.
- If we want to change the configuration of any part of the workflow, we need to do it manually, which is a much more time-consuming process.
For solving all the above problems, we can use a Machine learning pipeline. With the ML pipeline, each part of the workflow acts as an independent module. So whenever we need to change any part, we can choose that specific module and use that as per our requirement.

### Example:
Building any ML model requires a huge amount of data to train the model. As data is collected from different resources, it is necessary to clean and pre-process the data, which is one of the crucial steps of an ML project. However, whenever a new dataset is included, we need to perform the same pre-processing step before using it for training, and it becomes a time-consuming and complex process for ML professionals.

To solve such issues, ML pipelines can be used, which can remember and automate the complete pre-processing steps in the same order.


## The stages of a machine learning pipeline
- **Data collection:** In this initial stage, new data is collected from various data sources, such as databases, APIs or files. This data ingestion often involves raw data which may require preprocessing to be useful.
- **Data preprocessing:** This stage involves cleaning, transforming and preparing input data for modeling. Common preprocessing steps include handling missing values, encoding categorical variables, scaling numerical features and splitting the data into training and testing sets.
- **Feature engineering:** Feature engineering is the process of creating new features or selecting relevant features from the data that can improve the model's predictive power. This step often requires domain knowledge and creativity.
- **Model selection:** In this stage, you choose the appropriate machine learning algorithm(s) based on the problem type (e.g., classification, regression), data characteristics, and performance requirements. You may also consider hyperparameter tuning.
- **Model training:** The selected model(s) are trained on the training dataset using the chosen algorithm(s). This involves learning the underlying patterns and relationships within the training data. Pre-trained models can also be used, rather than training a new model.
- **Model evaluation:** After training, the model's performance is assessed using a separate testing dataset or through cross-validation. Common evaluation metrics depend on the specific problem but may include accuracy, precision, recall, F1-score, mean squared error or others.
- **Model deployment:** Once a satisfactory model is developed and evaluated, it can be deployed to a production environment where it can make predictions on new, unseen data. Deployment may involve creating APIs and integrating with other systems.
- **Monitoring and maintenance:** After deployment, it's important to continuously monitor the model's performance and retrain it as needed to adapt to changing data patterns. This step ensures that the model remains accurate and reliable in a real-world setting.

## Benefits of Machine Learning Pipelines
- Unattended runs
- Easy debugging
- Easy tracking and versioning
- Fast execution
- Collaboration
- Reusability
- Heterogenous Compute

## Considerations while building a Machine Learning Pipeline
- **Create each step as reusable components:** We should consider all the steps that involve in an ML workflow for creating an ML model. Start building a pipeline with how data is collected and pre-processed, and continue till the end. It is recommended to limit the scope of each component to make it easier to understand and iterate.
- **Always codify tests into components:** Testing should be considered an inherent part of the pipeline. If you, in a manual process, do some checks on how the input data and the model predictions should look like, you should codify this into a pipeline.
- **Put all the steps together:** We must put all the steps together and define the order in which components of the workflow are processed, including how input and outputs run through the pipeline.
- **Automate as per needed:** When we create a pipeline, it already makes the workflow automated as it manages and handles the different running steps of workflow without any human intervention. However, various people's aim is to make the complete pipeline automated when specific criteria are met. For example, you may monitor model drift in production to trigger a re-training run or - simply do it more periodically, like daily.
