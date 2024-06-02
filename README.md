# Data Analysis of Independence days of countries

This repository contains an analysis of countries' independence data, focusing on various dimensions such as the year of independence, continent, and colonial powers. The dataset provides valuable insights into historical trends and geopolitical shifts. Below is an outline of the key analyses and SQL queries performed.

## Dataset Description
The dataset includes the following columns:

1. Country: Name of the country.
2. Continent: Continent to which the country belongs.
3. Year: The year the country gained independence.
4. Month: The month the country gained independence.
5. Day: The specific day of independence.
6. Independence from: The colonial power from which the country gained independence

## Data Analysis

### 1. Total Countries
Total number of countries in dataset

```sql
  select count(country)countries
  from independence_data;
```

![01](https://github.com/MoaviaMahmood/Independence-days-of-countries/assets/168455506/c60c1ae1-b0e9-4fb4-a57a-1c0238ae1aed)

### 2. Countries Per Continent
Number of countries per contries in dataset 

```sql
  SELECT continent AS Continent, COUNT(*) AS Countries
  FROM     independence_data
  GROUP BY continent;
```

![02](https://github.com/MoaviaMahmood/Independence-days-of-countries/assets/168455506/b6040454-2fb8-491d-a75e-6e89167528e9)

### 3. Independence Per Month
Number of Countries independence per month 

```sql
  select month,
		count(country) as countries
  from independence_data
  group by month
  order by countries desc;
```

![03](https://github.com/MoaviaMahmood/Independence-days-of-countries/assets/168455506/4ad0b5e7-e436-4ce2-9809-66a2cabc900f)

### 4. 20th Century Independence
Countries gain independence in 20th century  

```sql
  select * 
  from independence_data
  where year like '19%'
  order by year;
```

![4 1](https://github.com/MoaviaMahmood/Independence-days-of-countries/assets/168455506/7f678f26-cdaa-4f0b-8a7f-e1dfd2a551c5)
![4 2](https://github.com/MoaviaMahmood/Independence-days-of-countries/assets/168455506/e056ff73-e36f-496c-bb4c-0454591db1e2)
![4 3](https://github.com/MoaviaMahmood/Independence-days-of-countries/assets/168455506/b27f0bdf-bd95-489a-880a-4ddd0f57c04b)
![4 6](https://github.com/MoaviaMahmood/Independence-days-of-countries/assets/168455506/75e5907a-7a21-4069-97e9-772a309e2b66)
![4 4](https://github.com/MoaviaMahmood/Independence-days-of-countries/assets/168455506/277cd672-1154-49ca-8ded-ccdbff299c37)
![4 5](https://github.com/MoaviaMahmood/Independence-days-of-countries/assets/168455506/68e78505-58ed-4164-a65d-02d69362acf0)




