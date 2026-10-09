# Medical Appointment No-Show Analysis

Exploratory analysis of 110,527 medical appointments from Brazil, focused on attendance patterns and factors associated with patient no-shows.

## Objectives

- Assess the dataset's completeness and consistency.
- Clean invalid values and prepare date fields for analysis.
- Explore attendance patterns by neighbourhood, age and gender.
- Compare attendance rates for patients who did and did not receive an SMS.
- Communicate findings together with important limitations.

## Dataset

The dataset contains appointment-level information including:

- Patient and appointment identifiers
- Scheduling and appointment dates
- Age and gender
- Neighbourhood
- Selected health indicators
- Scholarship participation
- SMS receipt
- Appointment attendance

## Analysis workflow

1. Inspect column types, missing values and duplicates.
2. Convert date fields to datetime values.
3. Remove the invalid age value of `-1`.
4. Standardize the no-show column for easier analysis.
5. Calculate descriptive summaries and attendance distributions.
6. Visualize patterns with Matplotlib.

## Questions explored

- Which neighbourhoods account for the most appointments?
- How does attendance vary across age groups?
- How do attendance proportions compare by gender?
- What association is visible between SMS receipt and attendance?

## Technologies

- Python
- pandas
- Matplotlib
- Jupyter Notebook

## Repository structure

- `investigate-a-dataset.ipynb` — cleaning, exploratory analysis and visualizations
- `noshowappointments-kagglev2-may-2016.csv` — source dataset
- `requirements.txt` — Python dependencies

## Running the analysis

```bash
python -m venv .venv
pip install -r requirements.txt
jupyter notebook
```

Open `investigate-a-dataset.ipynb` and run the cells in order.

## Limitations

- The analysis is observational and cannot establish causation.
- Appointment counts differ substantially between demographic groups, so raw counts must be interpreted alongside proportions.
- The dataset does not include every factor that may affect attendance, such as appointment purpose, travel distance or individual communication preferences.
- Any observed relationship between SMS receipt and attendance may be influenced by other variables.

## Data source

The analysis uses the public **Medical Appointment No Shows** dataset from Kaggle.

