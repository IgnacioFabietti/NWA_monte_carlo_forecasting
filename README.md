# A&E Demand in Peterborough and Huntingdon to 2040 Forecast

![image](https://github.com/user-attachments/assets/b47172bf-f1e0-48eb-96f3-db3a88eb7418)

### Table Of Contents

- [A&E Demand in Peterborough and Huntingdon to 2040 Forecast](#a-e-demand-in-peterborough-and-huntingdon-to-2040-forecast)
    + [Table Of Contents](#table-of-contents)
    + [Background](#background)
      - [Why is it important?](#why-is-it-important-)
    + [Goal](#goal)
    + [Methods & Results](#methods---results)
      - [Collaborative Approach](#collaborative-approach)
      - [Forecasting Methodology](#forecasting-methodology)
      - [Results](#results)
    + [Recommendations](#recommendations)
    + [Future Work](#future-work)
    + [Data Dictionaries](#data-dictionaries)
    + [Contact Information](#contact-information)

### Background

Bed occupancy rate remains a critical parameter for evaluating hospital utilisation. It serves as a management indicator that provides insights into the hospital’s service capacity, helping assess space utilisation and resource allocation.

#### Why is it important?

Forecasting A&E attendances until 2040 is essential for effective healthcare planning, cost management, and resource allocation. With an ageing population, an increasing prevalence of chronic conditions, and growing demand for emergency services, accurate projections enable NHS trusts to anticipate future pressures and optimise staffing, infrastructure, and budgets. By understanding trends and drivers of A&E demand—such as population growth and socioeconomic changes—local authorities can design targeted interventions to reduce avoidable attendances, such as improving access to GP services or investing in preventative care. This proactive approach ensures timely, high-quality patient care while minimising unnecessary expenditure, contributing to a more efficient and sustainable healthcare system.

### Goal

Accurately forecast yearly A&E attendances until 2040. Ultimately, the predictions aim to support NHS trusts in better resource utilisation, ensuring workforce and infrastructure planning aligns with projected demands.

### Methods & Results

#### Collaborative Approach

The success of any forecasting model lies not just in its technical accuracy but also in its ability to drive actionable insights. Stakeholders don’t ask for “models”; they want solutions that enable better decision-making and increased organisational readiness. Thus, the first step involves collaborating with stakeholders to define the business intelligence requirements behind the forecasting question, such as:

-   Planning workforce and infrastructure.
    
-   Understanding population growth and demographics.
    
-   Financial and resource allocation.
    

#### Forecasting Methodology

Monte Carlo simulation was chosen for its ability to model uncertainty by generating a range of possible outcomes. This approach is well-suited for long-term forecasting, where variability and complex factors like population growth and demand fluctuations must be accounted for.

-   **Inputs:** Historical A&E total attendances at Northwest Anglia NHS Foundation Trust (scraped from NHS England statistical work) and Cambridgeshire County Council’s population estimates and forecasts.
    
-   **Exclusions:** Covid-19 years excluded to avoid skewing trends.
    
-   **Simulation Process:** Growth rates for attendance were randomly sampled from historical data (mean and standard deviation) and used to simulate 10,000 different potential future scenarios.
    
-   **Population Growth:** Attendance projections were adjusted based on forecasted population growth, applying a logarithmic function to mimic saturation.
    

#### Results
![image](https://github.com/user-attachments/assets/655d01b5-cd9f-4f0a-bdc8-94dcc722618e)

In Table format:
| Scenarios                  | 2025 | 2030 | 2035 | 2040 |
| -------------------------- | ---- | ---- | ---- | ---- |
| Optimistic (Mean - 1σ)  | 0% | \-2%   | \-4%  | \-7%  |
| Neutral (Mean)          | 8%   | 56%  | 100% | 128% |
| Pessimistic (Mean + 1σ) | 17%  | 114% | 205% | 264% |

The model’s output can provide scenario-driven insights (optimistic, neutral, pessimistic) that enable stakeholders to:

-   Align workforce planning with projected demand.
    
-   Scale capacity infrastructure appropriately.
    
-   Improve patient flow across services.
    

### Recommendations

-   **Validation:** Building confidence in the model through thorough validation of predictions.
    
-   **Scenario Planning:** Implementing scenario modelling to communicate results effectively.
    
-   **Further Model Improvements:** Including activity mitigators, planned service changes, and other factors.
    
-   **Generalisability:** This model can be adapted to other NHS trusts, making it a valuable reusable analytical pipeline (RAP).
    

### Future Work

The next step involves collaborating with stakeholders to translate predictions into actionable strategies and ensure the organisation’s future readiness. For example, utilising the New Hospitals Programme developed by the Strategy Unit to project future activity levels and capacity requirements.

### Data Dictionaries

The dataset is organised in a single CSV file. The structure includes:

| Date       | A&E attendances Type 1 | A&E attendances Type 2 | A&E attendances Other A&E Department | Total A&E attendances |
| ---------- | ---------------------- | ---------------------- | ------------------------------------ | --------------------- |
| 01/06/2015 | 7,036                  | 0                      | 773                                  | 7809|         

-   **Date:** Date of record.
    
-   **A&E attendances Type 1:** Major A&E units with a consultant-led 24-hour service.
    
-   **A&E attendances Type 2:** Single specialty A&E services (e.g., ophthalmology or dental).
    
-   **A&E attendances Other A&E Department:** Includes walk-in centres and minor injury units.
    
-   **Total A&E attendances:** Sum of all attendance types.
    

### Contact Information

For further details or access to the Python script, please contact: **Marcos Fabietti** Email: mifabietti@outlook.com
