# Titanic Survival Analysis in R

An exploratory data analysis (EDA) of the classic Titanic dataset using **R** and **R Markdown**, investigating how passenger demographic and socio-economic factors (specifically **Sex** and **Passenger Class**) influenced survival outcomes.

---

## 📋 Table of Contents
- [Overview](#overview)
- [Project Structure](#project-structure)
- [Methodology & Workflow](#methodology--workflow)
- [Key Analysis & Findings](#key-analysis--findings)
  - [1. Survival Analysis by Sex](#1-survival-analysis-by-sex)
  - [2. Survival Analysis by Passenger Class](#2-survival-analysis-by-passenger-class)
- [Technologies & Packages Used](#technologies--packages-used)
- [How to Run the Code](#how-to-run-the-code)
- [Authors](#authors)

---

## 📌 Overview
During the sinking of the Titanic, survival rates varied significantly among different passenger demographics. This project utilizes R to perform categorical data analysis on the built-in `Titanic` dataset. By constructing cross-tabulations, generating comparative visualizations, and conducting formal statistical hypothesis tests (Chi-Square Test of Independence), we determine whether survival was independent of sex and ticket class.

---

## 📁 Project Structure

```text
.
├── Titanic Survival Analysis.Rmd  # Main R Markdown source file
├── README.md                      # Project documentation
└── Titanic_Survival_Analysis.html # Rendered HTML report (generated upon knitting)
```

---

## ⚙️ Methodology & Workflow

1. **Data Reconstruction**: Convert R's built-in 4-dimensional contingency array (`Titanic`) into a flat, individual-level dataset (`data.frame`) preserving frequency counts.
2. **Descriptive Summaries**: Build contingency tables (`table()`) to examine raw survival counts across subgroups.
3. **Data Visualization**: Create grouped bar charts (`barplot()`) to visually evaluate survivor vs. non-survivor distributions.
4. **Hypothesis Testing**: Execute **Chi-Square Tests of Independence** (`chisq.test()`) to evaluate the statistical dependence between factors and survival.

---

## 📊 Key Analysis & Findings

### 1. Survival Analysis by Sex
* **Hypothesis**:
  * $H_0$: Survival and Sex are independent.
  * $H_1$: Survival and Sex are dependent.
* **Result**: The Chi-square test produced an extremely small $p$-value ($p < 0.05$). We reject the null hypothesis, confirming statistically significant evidence that female passengers had a significantly higher likelihood of survival ("women and children first" policy).

### 2. Survival Analysis by Passenger Class
* **Hypothesis**:
  * $H_0$: Survival and Passenger Class (1st, 2nd, 3rd, Crew) are independent.
  * $H_1$: Survival and Passenger Class are dependent.
* **Result**: The test confirms $p < 0.05$, rejecting the null hypothesis. Ticket class heavily influenced survival chances, with upper-class passengers gaining prioritized access to lifeboats.

---

## 🛠️ Technologies & Packages Used
- **Language**: R
- **Format**: R Markdown (`.Rmd`)
- **Graphics & Statistics**: Base R (`barplot`, `table`, `chisq.test`)
- **Rendering**: `knitr` & `rmarkdown`

---

## 🚀 How to Run the Code

1. **Clone the repository**:
   ```bash
   git clone https://github.com/your-username/titanic-survival-analysis.git
   cd titanic-survival-analysis
   ```

2. **Open in RStudio**:
   Open `Titanic Survival Analysis.Rmd` in RStudio.

3. **Knit the Report**:
   Click the **Knit** button in RStudio or run the following R command in your console:
   ```R
   rmarkdown::render("Titanic Survival Analysis.Rmd")
   ```

---

## 👥 Authors
* **MD. Mehedi**
* **Tanjena Akter Shefa**
* **Shahriyar Hoque Fihal**
