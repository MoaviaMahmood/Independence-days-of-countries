# Data Analysis of Independence days of countries
## Description
This repository contains an analysis of countries' independence data, focusing on various dimensions such as the year of independence, continent, and colonial powers. The dataset provides valuable insights into historical trends and geopolitical shifts. Below is an outline of the key analyses and SQL queries performed.

## Dataset

The dataset includes the following columns:

1. Country: Name of the country.
2. Continent: Continent to which the country belongs.
3. Year: The year the country gained independence.
4. Month: The month the country gained independence.
5. Day: The specific day of independence.
6. Independence from: The colonial power from which the country gained independence

# Data Analysis

## 1. Total Countries
Total number of countries in dataset

```sql
select count(country) countries
from independence_data;
```

![01](https://github.com/MoaviaMahmood/Independence-days-of-countries/assets/168455506/c60c1ae1-b0e9-4fb4-a57a-1c0238ae1aed)

## 2. Countries Per Continent
Number of countries per contries in dataset 

```sql
SELECT continent AS Continent,
	COUNT(*) AS Countries
FROM independence_data
GROUP BY continent;
```

![02](https://github.com/MoaviaMahmood/Independence-days-of-countries/assets/168455506/b6040454-2fb8-491d-a75e-6e89167528e9)

## 3. Independence Per Month
Number of Countries independence per month 

```sql
select month,
	count(country) as countries
from independence_data
group by month
order by countries desc;
```

![03](https://github.com/MoaviaMahmood/Independence-days-of-countries/assets/168455506/4ad0b5e7-e436-4ce2-9809-66a2cabc900f)

## 4. Earliest Independent Countries
Top 10 earliest countries to get independence

```sql
select top (10)*
from independence_data
where year not like 'NA'
order by year asc;
```
![5](https://github.com/MoaviaMahmood/Independence-days-of-countries/assets/168455506/fd41ae02-18e3-41a6-ac46-f092b4e5aed3)

## 5. Latest Independent Countries
Top 10 latest countries to get independence

```sql
select *
from independence_data
where year like '20%'
order by year desc;
```
![6](https://github.com/MoaviaMahmood/Independence-days-of-countries/assets/168455506/7f929530-5aab-487a-9084-d50e4b98dedf)

## 6. Colonial Powers
Top 10 colonial powers in the world 

```sql
SELECT top (10)
    independence_from AS Colonial_Power, 
    COUNT(*) AS CountryCount
FROM 
    independence_data
where independence_from not like 'NA' 
GROUP BY 
    independence_from
order by
	CountryCount desc;
```
![7](https://github.com/MoaviaMahmood/Independence-days-of-countries/assets/168455506/7e78b3bc-acfb-42f2-89ed-b31728ab1f66)

## 7. Independence Per Century
Number of Countries gain independence per century  

```sql
SELECT 
    (Year/100)*100 AS Decade, 
    COUNT(*) AS CountryCount
FROM 
    independence_data
where year not like 'NA'
GROUP BY 
    (Year/100)*100
ORDER BY 
    Decade desc;
```
![8](https://github.com/MoaviaMahmood/Independence-days-of-countries/assets/168455506/78dd7a6a-e9c2-46da-bc61-99eaa9721f0c)

## 8. Independence from UK
Number of Countries gain independence from United Kingdom  

```sql
select *
from independence_data
where independence_from like 'United Kingdom'
order by year;
```
![9 1](https://github.com/MoaviaMahmood/Independence-days-of-countries/assets/168455506/7e1a5791-bd1c-4881-97c4-d4d22af43f1e)
![9 2](https://github.com/MoaviaMahmood/Independence-days-of-countries/assets/168455506/12e41b05-ef04-486f-afa8-2c15dee8914b)

## 8. Independence in August
Countries gain independence in August 

```sql
select *
from independence_data
where month like 'August'
order by year;
```
![10](https://github.com/MoaviaMahmood/Independence-days-of-countries/assets/168455506/2d3638d2-33c8-485b-966b-3e91b7cc0e3c)


## 10. 20th Century Independence
Countries gain independence in 20th century  

```sql
	select * 
	from independence_data
	where year like '19%'
	order by year;
```

![4 1](https://github.com/MoaviaMahmood/Independence-days-of-countries/assets/168455506/dadbd9ec-79c1-42eb-a618-e11cbf7f5ab8)
![4 2](https://github.com/MoaviaMahmood/Independence-days-of-countries/assets/168455506/8657a646-6617-4c49-ad4b-ab45c22ebdc2)
![4 3](https://github.com/MoaviaMahmood/Independence-days-of-countries/assets/168455506/8ac42d41-7b55-4d9b-b218-d7e95809a40a)
![4 4](https://github.com/MoaviaMahmood/Independence-days-of-countries/assets/168455506/c2d65cc8-3e72-47f8-b61f-7732e15fb9cd)
![4 5](https://github.com/MoaviaMahmood/Independence-days-of-countries/assets/168455506/9efd8bbc-67be-4d30-bcd3-d98c54a6d500)





