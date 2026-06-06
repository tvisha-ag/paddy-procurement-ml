# Predictive Procurement Optimization & MSP Allocation Inelasticity

An end-to-end machine learning pipeline that shifts public agricultural logistics from a reactive baseline model to a proactive, precision-driven supply chain. This project analyzes systemic geographical distribution variance and procurement inelasticity in state-sponsored crop procurement using raw government data.

## 📊 Core Architectural Highlights
* **Data Engineering (Unpivoting):** Developed an automated unpivoting routine in Python using `Pandas` to normalize high-dimensional, alternating horizontal wide-format government matrices into clean, relational, time-series records.
* **Exploratory Data Analysis (EDA):** Leveraged `Seaborn` to expose critical over-allocation trends in historical legacy zones and isolate public distribution supply chain vulnerability to macro-level imbalances.
* **Feature Engineering:** Extracted temporal autoregressive lag variables ($t-1$ procurement quantity) to capture and quantify regional supply chain dependencies on past institutional operational baselines.
* **Predictive Modeling:** Deployed a non-linear ensemble method (`RandomForestRegressor`) to effectively navigate highly skewed regional distribution variances without over-smoothing peak arrival vectors.

## 🚀 Technical Lifecycle & Pipeline Architecture
1. **Ingestion & Inlier Extraction:** Filters out summary statistical rows (e.g., national totals) and normalizes messy or truncated regional strings.
2. **Relational Melting:** Normalizes horizontal `Year | Qty | Value` schemas into uniform rows indexed by `[State, Financial_Year]`.
3. **Autoregressive Processing:** Generates the $t-1$ rolling shift parameters safely within geographic barriers to prevent data leakage.
4. **Ensemble Fitting & Interpretation:** Evaluates the features using a controlled 80/20 train-test split, scoring variance via the Coefficient of Determination ($R^2$).

## 📈 Key Empirical Results
* **Model Accuracy ($R^2$ Score):** Outperforms basic linear trends, successfully capturing complex geographical procurement variances.
* **Feature Importance:** Feature coefficients verify that macro-level agricultural procurement remains highly inelastic year-over-year, relying almost entirely on historical baselines (`Lag_1_Qty`) rather than dynamic regional allocation.