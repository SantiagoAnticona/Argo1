### NASA Space Apps Challenge: Predicting Emissions in Industrial Sectors

# **Project Overview**

This project was created as a solution for the [NASA Space Apps Challenge 2024](https://www.spaceappschallenge.org/). It focuses on building predictive models to estimate greenhouse gas emissions in key industrial sectors. This aligns with the broader challenge of addressing environmental sustainability and climate action through data-driven insights.

# **Problem Statement**

Greenhouse gas (GHG) emissions from industrial sectors significantly contribute to climate change. Monitoring and predicting these emissions is critical for setting policy targets, improving sustainability practices, and tracking compliance with international agreements like the Paris Agreement. However, the data available is often fragmented, making it difficult for governments and organizations to take timely and effective action.

This project leverages machine learning models trained on emission data from various industrial activities to address the following key objectives:

1. **Predict emissions** from diverse industrial sources with high accuracy.
2. **Provide insights** that help governments and companies make informed decisions to reduce their carbon footprint.
3. **Enable real-time data integration** for continuous monitoring and improved decision-making.

# **Selected Challenge**

The project fits into the **"Sustaining Our Planet for Future Generations"** challenge category. By developing a tool that can predict industrial emissions, this project empowers decision-makers to set clear targets and prioritize sectors where mitigation efforts would have the most significant impact.

# **Why This Project Matters**

Climate change is a global challenge, and the accurate prediction of GHG emissions is crucial to mitigating its impact. By harnessing machine learning and predictive analytics, we can model current emission patterns and provide governments and organizations with actionable insights to meet climate goals.

Our project directly supports the **UN Sustainable Development Goals (SDG 13: Climate Action)** by using data and AI to monitor environmental impact, reduce emissions, and help develop strategies for a more sustainable future.

# **Technical Approach**

Using datasets from diverse industrial sectors, including mining, aviation, and agriculture, we built predictive models using **CatBoost** to handle both numerical and categorical data effectively. The project involves:

- **Data Cleaning and Preprocessing:** Ensuring data consistency, handling missing values, and transforming categorical features.
- **Model Selection and Training:** Using **CatBoostRegressor** to train models on industrial emissions data.
- **Performance Metrics:** Evaluating model performance with metrics such as **Mean Squared Error (MSE)** and **R² Score**.

## **Selected Models**

We trained and optimized models on several critical datasets, achieving high accuracy for the following sectors:

| File                                           | MSE             | R² Score | Model Path                                                     |
|------------------------------------------------|-----------------|----------|----------------------------------------------------------------|
| cropland-fires_emissions_sources.csv           | 33,391,581,805  | 0.9794   | `models/cropland-fires_emissions_sources_model.pkl`            |
| manure-left-on-pasture-cattle_emissions.csv    | 5,864,650,057   | 0.9427   | `models/manure-left-on-pasture-cattle_emissions_sources_model.pkl` |
| enteric-fermentation-cattle-pasture_emissions.csv | 180,105,992,070  | 0.9636   | `models/enteric-fermentation-cattle-pasture_emissions_sources_model.pkl` |
| iron-mining_emissions_sources.csv              | 7,979,907,499   | 0.9343   | `models/iron-mining_emissions_sources_model.pkl`               |
| bauxite-mining_emissions_sources.csv           | 353,427,345     | 0.9749   | `models/bauxite-mining_emissions_sources_model.pkl`            |
| electricity-generation_emissions_sources.csv   | 66,814,488,643  | 0.9876   | `models/electricity-generation_emissions_sources_model.pkl`    |
| domestic-aviation_emissions_sources.csv        | 591,107,053     | 0.9901   | `models/domestic-aviation_emissions_sources_model.pkl`         |
| international-aviation_emissions_sources.csv   | 1,734,899,921   | 0.9953   | `models/international-aviation_emissions_sources_model.pkl`    |
| forest-land-fires_emissions_sources.csv        | 2,719,148,999,613 | 0.9760 | `models/forest-land-fires_emissions_sources_model.pkl`         |
| water-reservoirs_emissions_sources.csv         | 532,792,746     | 0.9743   | `models/water-reservoirs_emissions_sources_model.pkl`          |
| aluminum_emissions_sources.csv                 | 2,780,396       | 0.9996   | `models/aluminum_emissions_sources_model.pkl`                  |
| steel_emissions_sources.csv                    | 54,488,033      | 0.9992   | `models/steel_emissions_sources_model.pkl`                     |
| cement_emissions_sources.csv                   | 3,861,094       | 0.9990   | `models/cement_emissions_sources_model.pkl`                    |

# **How the Models Work**

The models predict **emission quantities** based on various industrial processes and activities. By feeding in data such as production levels, geographic location, and activity type, the models can estimate CO₂-equivalent emissions. Each model is tailored to a specific sector, providing precise predictions based on historical and contextual data.

# **How to Use the Models**

1. **Clone the repository:** `git clone https://github.com/your-repository`
2. **Install dependencies:** `pip install -r requirements.txt`
3. **Run predictions:** Upload your dataset to the web app or use the provided API to get emission predictions.

### Example Usage:
```bash
python predict.py --model-path models/aluminum_emissions_sources_model.pkl --input-file data/aluminum_test_data.csv
```

# **Challenges Faced**
- Handling missing and inconsistent data across multiple industrial sectors.
- Building accurate models in a short timeframe with limited computational resources.
- Ensuring that models generalize well across different regions and industrial practices.

# **Future Improvements**
- **Real-time prediction integration:** Connect live industrial data streams to continuously update emission forecasts.
- **Expand to more sectors:** Broaden the scope to include sectors such as waste management, forestry, and transportation.
- **Integrate user-friendly web interface:** Develop a more interactive platform for users to upload data and receive predictions instantly.

# **Conclusion**

This project provides a highly scalable and accurate method for predicting greenhouse gas emissions in various industrial sectors. By harnessing the power of machine learning and open data, it aims to help policymakers and organizations make more informed, data-driven decisions to combat climate change. 

We believe this submission aligns perfectly with the **NASA Space Apps Challenge 2024** goals, offering a robust solution to a global problem.
