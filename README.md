## World Database Exercise: 

<br>

#### Find USA Cities in Database 
    Select count(world.city.ID)
    FROM (world.city)
    LEFT JOIN (world.country)
    ON(world.city.CountryCode = world.country.Code)
    WHERE (world.city.CountryCode = 'USA')
    
    >274

#### Find out what the population and average life expectancy for people in Argentina (ARG) is!

    SELECT Population, LifeExpectancy,Name
    FROM `world`.`country`
    WHERE name = 'Argentina';

|Population|LifeExpectancy,| Name       |
|----------|---------------|------------|
|'37032000'|'75.1',        |'Argentina' |



Display all the cities for any country of your choice besides the USA

    Select world.city.CountryCode, world.city.Name, world.city.Population
    FROM (world.city)
    LEFT JOIN (world.country)
    ON(world.city.CountryCode = world.country.Code)
    WHERE (world.city.CountryCode = 'ARG')

2 more

Populations outside europe

    Select Continent, sum( Population)
    FROM (world.country)
    WHERE (Continent != 'Europe')
    Group By Continent;

List of All American countries, North and South, with full query info:

    Select *
    FROM (world.country)
    WHERE (Continent = 'North America' OR Continent = 'South America')
    Order By Continent, region, Name


