# Building Energy Analytics with Machine Learning

Commercial and institutional buildings account for about one‑fifth of global electricity consumption and greenhouse gas emissions, though day‑to‑day energy management often relies on static benchmarks and manual heuristics rather than automated or predictive analytics. This gap makes it difficult for facility managers and sustainability teams to react to daily high‑ or low‑load periods, optimize heating and cooling schedules, and quantify the potential impact of energy‑saving interventions. The problem this project addresses is that, although many machine learning techniques exist for building energy forecasting, organizations often lack clear, explainable examples that show how to apply them in practice and connect them to daily energy management decisions. This project develops and documents a concrete, explainable forecasting workflow that can serve as a template for organizational use.

In this project, historical building load data is combined with weather and calendar features to train and compare multiple regression algorithms, including baseline models, linear models, and tree‑based ensembles. Model performance is evaluated using metrics such as Root Mean Square Error (RMSE) and Mean Absolute Error (MAE), and interpretability techniques are applied to identify the most influential drivers of energy use. By demonstrating that machine learning can substantially improve short‑term load forecasts and by translating model outputs into potential cost and emissions savings, the project illustrates how data science can directly support energy efficiency, operational resilience, and ESG objectives in the built environment.

## Data

This project uses an open dataset containing historical energy consumption for an anonymized building located in Spain from 2016 to 2019, originally compiled by the Instituto Tecnológico de Santo Domingo. Hourly energy use is recorded using smart meters installed in the building.

For each timestamp, the dataset includes both whole‑building electricity consumption and a set of variables sourced from NASA’s Prediction Of Worldwide Energy Resources (POWER) API, along with holiday indicators for Spain. The main variables are:

- **ENERGY** – Whole‑building electricity consumption (kWh)
- **HDD18_3** – Heating degree days below 18.3 °C
- **CDD0**, **CDD10** – Cooling degree days above 0 °C and 10 °C
- **PRECTOT** – Precipitation (mm/hour)
- **RH2M** – Relative humidity at 2 m (%)
- **T2M**, **T2M_MIN**, **T2M_MAX** – Air temperature at 2 m (°C), and its hourly minimum and maximum
- **ALLSKY** – All‑sky surface longwave downward irradiance (W/m²)
- **HOLIDAY** – Binary flag indicating public holidays in Spain

These features provide the basis for building short‑term forecasting models that link building load to atmospheric conditions and holiday behavior.

Citation: Mariano, Deyslen (2024), *Building Energy Consumption Data*, Mendeley Data, V2, doi: 10.17632/mzkyh37mtr.2
