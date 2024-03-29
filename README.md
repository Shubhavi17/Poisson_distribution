# Fitting Poisson  distribution
# Aim : 

To fit poisson distribution for the arrival of objects per minute from the feeder

# Software required :  

Python and Visual component tool

# Theory:

The Poisson distribution is the discrete probability distribution of the number of events occurring in a given time period, given the average number of times the event occurs over that time period.

![image](https://user-images.githubusercontent.com/104613195/166248326-fd042076-8b0b-40c4-8b11-1d8e8fcb74db.png)

 Conditions for Poisson Distribution:

1. An event can occur any number of times during a time period.
2. Events occur independently. I
3. The rate of occurrence is constant.
4. The probability of an event occurring is proportional to the length of the time period. 
 
# Procedure :

![image](https://user-images.githubusercontent.com/104613195/166251988-d0c53205-6080-4f7b-ae4c-398178586637.png)

# Experiment :

![image](https://user-images.githubusercontent.com/103921593/230282876-f4a5afbf-cac1-4648-a1b0-c78840638a8e.png)

# Program :
*/
```
import numpy as np
from scipy.stats import poisson
from scipy.optimize import curve_fit

# Example data: Number of objects arriving per minute
arrivals_per_minute = [2, 4, 3, 5, 6, 2, 3, 4, 5, 2, 3, 4, 5]

# Define the Poisson probability mass function
def poisson_pmf(x, mu):
    return poisson.pmf(x, mu)

# Fit the Poisson distribution to the data
mu, _ = curve_fit(poisson_pmf, np.arange(len(arrivals_per_minute)), arrivals_per_minute)

print("Fitted Poisson Lambda (Mean):", mu[0])
```
# Output : 

![Screenshot 2024-03-29 195102](https://github.com/Shubhavi17/Poisson_distribution/assets/150005085/a19e30e4-7b6d-4266-a8f1-91ab6ef87603)



# Results

The Poisson distribution is fitted for the objects arrived from feeder per minute and the data is tested using Chi-square test. 
 
