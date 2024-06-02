# Data Analysis of Independence days of countries

This repository contains an analysis of countries' independence data, focusing on various dimensions such as the year of independence, continent, and colonial powers. The dataset provides valuable insights into historical trends and geopolitical shifts. Below is an outline of the key analyses and SQL queries performed.

## Dataset Description
The dataset includes the following columns:

#### Country: Name of the country.
#### Continent: Continent to which the country belongs.
#### Year: The year the country gained independence.
#### Month: The month the country gained independence.
#### Day: The specific day of independence.
#### Independence from: The colonial power from which the country gained independence

### 1. Total Countries

#### Total number of countries in dataset

```sql
  select count(country)countries
  from independence_data;
```

![01](https://github.com/MoaviaMahmood/Independence-days-of-countries/assets/168455506/c60c1ae1-b0e9-4fb4-a57a-1c0238ae1aed)

