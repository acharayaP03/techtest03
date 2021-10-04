<h1 align="center">Lyka Tech Test with laravel</h1>

## About Laravel project

This project is built with maatwebsite/excel package which reads data provided in csv or excel formate.

- first clone project on your working dir then run `composer install`
- create .env and copy .env.example by running following command `cp .env.example .env`.
- set your local dev database as follows while replacing dbname, username and password as you desire, 
    ```
        DB_CONNECTION=mysql
        DB_HOST=127.0.0.1
        DB_PORT=3306
        DB_DATABASE=yourdbname 
        DB_USERNAME=username 
        DB_PASSWORD=password 
     ```
    
- Then run the following migrate command to create user and user-events table
    ```
        php artisan migrate
        
    ```
- Then run the seed command to seed the tables from the csv file.
    ```
        php artisan db:seed
    ```
- Once the db is seeded, we can run server `php artisan serve`.


## Possible api endpoints
- ` http://127.0.0.1:8000/api/users ` to get all users 
- `http://127.0.0.1:8000/api/user-events/2 ` to get user events
- `http://127.0.0.1:8000/api/user-event-groups/234` to get events by group

