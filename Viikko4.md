Koostetieto kyselyt

1. select max(elevation_ft)
    -> from airport;

    ![Harjoitustehtävä 1](Viikko4_koostetieto_1.png)

2. select continent, count(*)
    -> from country
    -> group by continent;

    ![Harjoitustehtävä 2](Viikko4_koostetieto_2.png)

3. select screen_name, count(*)
    -> from game, goal_reached
    -> where game.id = goal_reached.game_id
    -> group by screen_name;

    ![Harjoitustehtävä 3](Viikko4_koostetieto_3.png)

4. select screen_name
    -> from game
    -> order by co2_consumed ASC
    -> limit 1;

    ![Harjoitustehtävä 4](Viikko4_koostetieto_4.png)

5. select country.name, count(*)
    -> from country, airport
    -> where country.iso_country = airport.iso_country
    -> group by country.name
    -> order by count(*) desc
    -> limit 50;

    ![Harjoitustehtävä 5](Viikko4_koostetieto_5.png)

6. select country.name
    -> from airport, country
    -> where airport.iso_country = country.iso_country
    -> group by country.iso_country
    -> having count(*) > 1000
    -> order by country.iso_country;

    ![Harjoitustehtävä 6](Viikko4_koostetieto_6.png)
