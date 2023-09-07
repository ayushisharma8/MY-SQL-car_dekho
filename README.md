# MY-SQL-car_dekho

Create schema cars;

use cars;

# Read data
select * from car_dekho;

# Total cars: To get a total count of total records.--
select count(*) from car_dekho;

# The manager asked the employee, How many cars will be available in 2023?--
select count(*) from car_dekho where year=2023;

# The manager asked the employee, how many car is available in 2020,2021,2023?--
select  year, count(*) from car_dekho where year in (2020,2021,2022) group by year;

# Client asked me to print the total of all cars by year. I don't see all the details.
select year, count(*) from car_dekho group by year;

# Client asked to car dealer agent, how many diesel cars will be there in 2020?--
select year, count(*) from car_dekho where year=2020 and fuel="Diesel";#20

# Client asked to car dealer agent, how many Petrol cars will be there in 2020?--
select year, count(*) from car_dekho where year=2020 and fuel="Petrol";#51
 
 # Print of all the fuel cars (Petrol, Diesel and CNG) come by all year---
select year, count(*) from car_dekho where fuel in ("Petrol") group by year;
select year, count(*) from car_dekho where fuel in ("Diesel") group by year;
select year, count(*) from car_dekho where fuel in ("CNG") group by year;

# Manager said that there were more than 100 cars in a given year, which year had a more than 100 cars?--
select  year ,count(*) from car_dekho group by year having count(*)>100 ;

# All cars count details between 2015 and 2023; we need a complete list---
select count(*) from car_dekho where year between 2015 and 2023;

# All cars details between 2015 and 2023; we need a complete list---
select * from car_dekho where year between 2015 and 2023;

# End---
