import pandas as pd
from matplotlib import pyplot as plt

data = pd.read_csv('countries.csv')
us = data[data.country == 'United States']

china = data[data.country == 'China']

plt.plot(us.year, us.population / 10**6)
plt.plot(china.year, china.population / 10**6)
plt.xlabel('year')
plt.ylabel('population')
plt.show()

us.population
us.population / us.population.iloc[0] * 100

plt.plot(us.year, us.population / us.population.iloc[0] * 100)
plt.plot(china.year, china.population / china.population.iloc[0] * 100
plt.legend(['United States', 'China'])
plt.xlabel('year')
plt.ylabel('population growth (first year = 100)')
plt.show()
