# Data Description

Data was collected from ICU patients in two separate hospital systems A and B.
The data for each patient is contained within a single pipe-delimited text file.
Each file das the same header and each row represents a single hour's worth of data.
Available patient co-variates consist of Demographics, Vital Signs, and Laboratory values, which are defined in the table below.

Sepsis-3 clinical criteria were applied for sepsis onset.
These imply a two-point change in the patient's Sequential Organ Failure Assessment (SOFA) score
and clinical suspicion of infection (as defined by the ordering of blood cultures or IV antibiotics).
The following time points are defined for each patient:

- $t_\text{suspicion}$:
	Clinical suspicion of infection identified as the earlier timestamp of IV antibiotics and blood cultures within a specified duration.
	1. If antibiotics were given first, then the cultures must have been obtained within 24 hours.
		If cultures were obtained first, then antibiotic must have been subsequently ordered within 72 hours.
	1. Antibiotics must have been administered for at least 72 consecutive hours to be considered.
- $t_\text{SOFA}$:
	The occurrence of end organ damage as identified by a two-point deterioration in SOFA score within a 24-hour period.
- $t_\text{sepsis}$:
	The onset time of sepsis is the earlier of $t_\text{suspicion}$ and $t_\text{SOFA}$
	as long as $t_\text{SOFA}$ occurs no more than 24 hours before or 12 hours after $t_\text{suspicion}$;
	otherwise, the patient is not marked as a sepsis patient.
	Specifically, if $t_\text{suspicion}- 24 \leq t_\text{SOFA} \leq t_\text{suspicion} + 12$,
	then $t_\text{sepsis} = \min (t_\text{suspicion}, t_\text{SOFA})$.

Patient records were truncated after ICU discharge,
and patients with more than 2 weeks of hourly time windows were truncated to 2 weeks.

| Column name   | Description                             |
|---------------|-----------------------------------------|
| **Vital signs** | **(columns 1-8)** |
| HR            | Heart rate (beats per minute)           | 
| O2Sat         | Pulse oximetry (%)                      | 
| Temp          | Temperature (Deg C)                     | 
| SBP           | Systolic BP (mm Hg)                     | 
| MAP           | Mean arterial pressure (mm Hg)          | 
| DBP           | Diastolic BP (mm Hg)                    | 
| Resp          | Respiration rate (breaths per minute)   | 
| EtCO2         | End tidal carbon dioxide (mm Hg)        |
| **Laboratory values** | **(columns 9-34)** |
| BaseExcess    | Measure of excess bicarbonate (mmol/L)  |
| HCO3          | Bicarbonate (mmol/L)                    |
| FiO2          | Fraction of inspired oxygen (%)         |
| pH            | N/A                                     |
| PaCO2         | Partial pressure of carbon dioxide from arterial blood (mm Hg) |
| SaO2          | Oxygen saturation from arterial blood (%) |
| AST           | Aspartate transaminase (IU/L)           |
| BUN           | Blood urea nitrogen (mg/dL)             |
| Alkalinephos  | Alkaline phosphatase (IU/L)             |
| Calcium       | (mg/dL)                                 |
| Chloride      | (mmol/L)                                |
| Creatinine    | (mg/dL)                                 |
| Bilirubin\_direct | Bilirubin direct (mg/dL)            |
| Glucose       | Serum glucose (mg/dL)                   |
| Lactate       | Lactic acid (mg/dL)                     |
| Magnesium     | (mmol/dL)                               |
| Phosphate     | (mg/dL)                                 |
| Potassium     | (mmol/L)                                |
| Bilirubin\_total | Total bilirubin (mg/dL)              |
| TroponinI     | Troponin I (ng/mL)                      |
| Hct           | Hematocrit (%)                          |
| Hgb           | Hemoglobin (g/dL)                       |
| PTT           | partial thromboplastin time (seconds)   |
| WBC           | Leukocyte count (count/nL)              |
| Fibrinogen    | (mg/dL)                                 |
| Platelets     | (count/nL)                              |
| **Demographics** | **(columns 35-40)** |
| Age           | Years (100 for patients 90 or above)    |
| Gender        | Female (0) or Male (1)                  |
| Unit1         | Administrative identifier for ICU unit (MICU)  |
| Unit2         | Administrative identifier for ICU unit (SICU)  |
| HospAdmTime   | Hours between hospital admit and ICU admit |
| ICULOS        | ICU length-of-stay (hours since ICU admit) |
| **Outcome** | **(column 41)** |
| SepsisLabel   | For sepsis patients, 1 if $t \geq t_\text{sepsis} - 6$ and 0 if $t < t_\text{sepsis} - 6$. For non-sepsis patients, 0. |

---

Sources:
- <https://github.com/physionetchallenges/physionetchallenges.github.io/blob/master/2019/index.md>
- Reyna et al, _Early Prediction of Sepsis From Clinical Data: The PhysioNet/Computing in Cardiology Challenge 2019_,
2019, Computing in Cardiology (CinC)
