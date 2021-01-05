# DatabasesChallenges

## World
1. Using COUNT, get the number of cities in the USA.

Answer: select count(id) from city where CountryCode='USA'; - 274


2. Find out the population and life expectancy for people in Argentina.

Answer: select Population, LifeExpectancy from country where Code='ARG'; - population: 37032000; life expectancy: 75.1


3. Using IS NOT NULL, ORDER BY, and LIMIT, which country has the highest life expectancy?

Answer: select Name, LifeExpectancy from country where LifeExpectancy is not null order by LifeExpectancy desc limit 1; - name: Andorra; life expectancy 83.5


~~4. Using JOIN ... ON, find the capital city of Spain.~~


~~5. Using JOIN ... ON, list all the languages spoken in the Southeast Asia region.~~


6. Using a single query, list 25 cities around the world that start with the letter F.

Answer: select Name from city where name like 'F%' limit 25 - Fagatogo; Florencio Varela; Formosa; Francistown; Fortaleza; Feira de Santana; Franca; Florianopolis; Foz do Iguacu; Ferraz de Vasconcelos; Francisco Morato; Franco da Rocha; Fuenlabrada; Faridabad; Firozabad; Farrukhabad-cum-Fatehgarh; Faizabad; Fatehpur; Firenze; Foggia; Ferrara; Forli; Fukuoka; Funabashi; Fukuyama


~~7. Using COUNT and JOIN ... ON, get the number of cities in China.~~


8. Using IS NOT NULL, ORDER BY, and LIMIT, which country has the lowest population? Discard non-zero populations.

Answer: select name, population from country where population is not null limit 1; - name: Aruba; population: 103000


~~9. Using aggregate functions, return the number of countries the database contains.~~

~~Hint: use COUNT~~


10. What are the top ten largest countries by area?

Answer: select name, surfacearea from country order by surfacearea desc limit 10; names: Russian Federation, Antarctica, Canada, China, United States, Brazil, Australia, India, Argentina, Kazakhstan; Surface Area: 17075400,00, 13120000.00, 9970610.00, 9572900,00, 9363520.00, 8547403.00, 7741220.00, 3287263.00, 2780400.00, 2724900.00


11. List the five largest cities by population in Japan.

Answer: select name from city where countrycode='JPN' order by population desc limit 5; - Tokyo, Jokohama [Yokohama], Osaka, Nagoya, Sapporo


~~12. List the names and country codes of every country with Elizabeth II as its Head of State. You will need to fix the mistake first!~~


13. List the top ten countries with the smallest population-to-area ratio. Discard any countries with a ratio of 0.
focus on name, population/surafcearea AS ratio - beware alias (AS); use original format


14. List every unique world language.

Answer: select distinct from countrylanguage; - (there are 457 rows, won't answer in full for this one lol)


15. List the names and GNP of the world's top 10 richest countries.

Answer: select name, gnp from country order by gnp desc limit 10; - name: United States, Japan, Germany, France, United Kingdom, Italy, China, Brazil, Canada, Spain; 8510700.00, 3787042.00, 2133367.00, 1424285.00, 1378330.00, 1161755.00, 982268.00, 776739.00, 598862.00, 553233.00


~~16. List the names of, and number of languages spoken by, the top ten most multilingual countries.~~

~~Hint: country and countrylanguage tables, JOIN the two together (check notes), SELECT and shrink from there~~


~~17. List every country where over 50% of its population can speak German.~~

~~Hint: JOIN~~


18. Which country has the worst life expectancy? Discard zero or null values.

Answer: select name from country where lifeexpectancy is not null limit 1; - Aruba


~~19. List the top three most common government forms~~

~~Hint: COUNT and GROUP BY, using governmentform as the focus~~


~~20. How many countries have gained independence since records began?~~
