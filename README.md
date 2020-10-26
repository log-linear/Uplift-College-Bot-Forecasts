# College Bot Forecasts

In May of 2019, Uplift Education created an internal tool to determine the 
probability that an Uplift student would be accepted into a given college. 
The code for the forecasting process used is documented within the included 
__forecasts.ipynb__ file.

A deidentified version of the dashboard can be found [here](https://public.tableau.com/profile/victor.faner8540\#!/vizhome/CollegeBotdeidentified/Explorer).

# Notes
- Forecasts were generated using a Random Forests model
- Target: Final application status - accepted vs. rejected
- Predictors:
    - Internal:
        - Student's GPA (transformed to a 0-1 scale)
        - Student's highest composite ACT score (transformed to a 0-1 scale)
    - External (Collected from IPEDS: https://nces.ed.gov/ipeds/)
        - Institution's average admission rate
        - Institution's average 25th percentile ACT/SAT score (transformed to a 
        0-1 scale)
            - To account for schools that only reported one or the other, both 
            the SAT and ACT were first transformed to a 0-1 scale, and the higher of
            the two was used as a predictor
