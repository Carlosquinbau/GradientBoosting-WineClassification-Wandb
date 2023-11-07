# GradientBoosting-WineClassification-Wandb


Este repositorio contiene un proyecto de experimentación de ciencia de datos en Upgrade Hub. Utilizamos pesos y sesgos para ajustar y evaluar sistemáticamente los hiperparámetros de un clasificador de aumento de gradiente. El DataSet con el que estamos trabajando es el de Wine.

## Sobre Upgrade Hub

[Upgrade Hub](https://www.upgrade-hub.com/) Es una institución educativa dedicada a ofrecer programas de capacitación de alta calidad en tecnología y ciencia de datos.

## Resultados

Los resultados de la experimentación se pueden ver en detalle en siguiente enlace de WanDB. Esto incluye varias métricas de rendimiento, como la precisión, junto con los hiperparámetros utilizados para cada experimento.

🔗 [View Experimentation Results](https://api.wandb.ai/links/carlos-quintero-bautista/x31ys56l)

## Descripción del Problema

La tarea que nos ocupa es un ejemplo clásico de un problema de clasificación multiclase. Nuestro objetivo es predecir la categoría de vino en función de varios atributos fisicoquímicos. El conjunto de datos de Wine es un conjunto de datos de referencia común en la comunidad de aprendizaje automático.

## Dataset

El conjunto de datos Wine es un conjunto de datos disponible públicamente que contiene 178 muestras de vinos con 13 atributos diferentes, como contenido de alcohol, ácido málico, cenizas, etc. Hay tres clases que representan tres tipos diferentes de vinos. El conjunto de datos es muy adecuado para experimentos de clasificación.

## Experimentation

For this project, we utilize the Gradient Boosting Classifier, a powerful ensemble machine learning algorithm that builds on decision trees. It is particularly known for its effectiveness in classification problems.

To find the best model, we explore various combinations of hyperparameters such as learning rate, maximum depth of the trees, the number of estimators, etc. Through systematic experimentation, we aim to understand the effect of these hyperparameters on the model's performance and find the combination that yields the best results.

We integrate Weights & Biases into our experimentation pipeline, which allows us to log the hyperparameters and the performance metrics for each experiment. Weights & Biases provides us with an interactive dashboard where we can visualize and analyze the results.

## Hyperparameter Tuning and Best Model

During the experimentation process, we performed an extensive search over the hyperparameter space. A total of **384 different combinations** of hyperparameters were tested to find the model that yields the best performance. The hyperparameters that we tuned include:

- Learning rate
- Maximum depth of the trees
- Number of estimators
- Loss function
- Subsample fraction
- Minimum number of samples required to split an internal node
- Minimum number of samples required to be at a leaf node

This extensive search allowed us to explore a wide range of models and identify the combination of hyperparameters that optimizes the performance for this specific dataset.

The model with the best score achieved an accuracy of **0.9815**. This high level of accuracy indicates that the model is highly effective in classifying the wine samples correctly. The hyperparameters of the best model are as follows:

- Learning rate: 0.1
- Loss function: deviance
- Max depth: 3
- min_samples_leaf: 2
- min_samples_split: 2
- n_estimators: 50
- subsample: 1

This combination of hyperparameters allowed the Gradient Boosting Classifier to capture the underlying patterns in the data efficiently and make highly accurate predictions.

## Running the Code

To run the code, first, ensure you have all the dependencies installed:


## Contributions

Contributions to this repository are welcome. Please, ensure that the code follows best practices and is well-documented.

## License

This project is licensed under the MIT License.
