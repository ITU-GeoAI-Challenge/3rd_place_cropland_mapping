# GEO-AI Challenge for Cropland Mapping by ITU

![crop2](https://github.com/ITU-GeoAI-Challenge/3rd_place_cropland_mapping/assets/61426508/edc66ac5-5a51-468f-850a-0b33eb75729d)

Timely and accurate crop maps are essential for various applications in agriculture and other relevant research fields. However, the current cropland maps do not align with FAOSATA's definition of crops and arable lands. Furthermore, updating these maps to monitor changes over time poses significant challenges.

The goal of this challenge was to develop accurate and cost-effective classification models to improve the accuracy and robustness of land cover classification with satellite images.

## Software & Hardware Requirements
Google Colab was used for preprocessing, training, and inferencing stages. 

## Workflow Solution

```mermaid
graph TD
    A[Google Earth Engine] --> B(Sentinel-1)
    A --> C(Sentinel-2)
    A --> D(SMAP Level-4)

    B --> E(Vegetation Indices)
    C --> E
    
    E --> F(Dataset)
    D --> F
    F --> G(Training Dataset)
    F --> K(Testing Dataset)

    G --> M(Modeling: LGBM, Catboost )
    M --> N(Trained Models)

    N --> O(Inference)
    K --> O

    O --> P[Predictions]

```


## Get Started
The solution saved in the notebooks folder with the following expected running time: 

|Notebook|Running time|
|-----------|--------|
|Notebook 1 | 5 minutes|
|Notebook 2 | 3.5 houres|

### Notebook 1
Split the datasets into 3 regions as following: Sudan, Iran, and Afghanistan.

### Notebook 2
Extract data from GEE, feature engineering, modeling, and inference.
