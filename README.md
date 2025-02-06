# AgileReq-LLM-Hybrid
This repository contains the source code and implementation details for the research which integrates Large Language Models (LLMs) with the Fuzzy Best-Worst Method (FBWM) to enhance decision support in Agile Requirements Change Management (ARCM) within Global Software Development (GSD) environments

The script uses fuzzy membership functions to evaluate six criteria:

- **C1:** Integration  
- **C2:** Communication  
- **C3:** Project Administration  
- **C4:** Human Resources  
- **C5:** Technology Factors  
- **C6:** Time  

### Fuzzy Membership Functions

The following linguistic terms and corresponding fuzzy values are used:

- **Equally Important (EI):** `(1, 1, 1)`
- **Weakly Important (WI):** `(2/3, 1, 3/2)`
- **Fairly Important (FI):** `(3/2, 2, 5/2)`
- **Very Important (VI):** `(5/2, 3, 7/2)`
- **Absolutely Important (AI):** `(7/2, 4, 9/2)`

### How It Works

1. **Fuzzy Comparisons:**  
   The script defines two lists:
   - **MIC (Most Important Comparisons):** Compares each criterion to the expert's most important criterion.
   - **LIC (Least Important Comparisons):** Compares each criterion to the expert's least important criterion.

2. **Fuzzy BWM Calculation:**  
   The fuzzy BWM function (from the `pyDecision` package) is called with the MIC and LIC values to compute:
   - **Fuzzy Weights:** The triangular fuzzy numbers representing the relative weights.
   - **Crisp Weights:** Defuzzified values (rounded for clarity) that sum to 1.

3. **Output:**  
   The script prints both the fuzzy and crisp weights for each criterion in percentage form.

### Requirements

- Python 3.6 or later
- [pyDecision](https://pypi.org/project/pyDecision/)
- [numpy](https://pypi.org/project/numpy/)
