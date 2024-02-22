# Unemployment-Analysis-During-COVID-19
from scipy import stats

# Assume you have two arrays representing unemployment rates in two regions
unemployment_region_A = [5.2, 4.9, 5.5, 4.8, 5.1]
unemployment_region_B = [6.1, 5.8, 6.2, 5.9, 6.0]

# Perform independent samples t-test
t_statistic, p_value = stats.ttest_ind(unemployment_region_A, unemployment_region_B)

# Output the results
print("Independent Samples t-test:")
print("T-statistic:", t_statistic)
print("P-value:", p_value)

# Interpret the results
alpha = 0.05  # significance level
if p_value < alpha:
    print("Reject the null hypothesis: There is a significant difference in unemployment rates between Region A and Region B.")
else:
    print("Fail to reject the null hypothesis: There is no significant difference in unemployment rates between Region A and Region B.")
