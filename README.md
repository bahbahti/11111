Car rent service
================

	Database consists of 3 tables:
1. cars
2. customers
3. orders


Table "cars":
--------------

Column | Type | Nullable | Type of key | Constraints 
--- | --- | --- | --- | ---
id | integer |  NO | primary key | unique
name | character varying |  NO |  - |  -
cost | integer |  NO |  - |  -
storage | character varying |  NO |  - |  -
available_amount | integer | YES | - |  -
registration_number | integer | NO | - |  unique
color | character varying | NO | - |  -



Table "customers":
--------------

Column | Type | Nullable | Type of key | Constraints 
--- | --- | --- | --- | ---
id | integer |  NO |  primary key |  unique 
first_name | character varying |  NO |  composite key |  unique 
last_name | character varying |  NO |  composite key |  unique 
area_of_living | character varying |  NO |  - |  - 
discount | integer |  YES |  - |  - 
passport_number | bigint |  NO |  - |  unique 
phone_number | bigint |  YES |  - |  - 



Table "orders":
--------------

Column | Type | Nullable | Type of key | Constraints 
--- | --- | --- | --- | ---
order_id | integer |  NO |  primary key |  unique 
start_day | date |  NO |  - |  - 
end_day | date |  YES |  - |  - 
amount_of_rent_cars | integer |  NO |  - |  - 
car_id | integer |  NO |  foreign key ( car_id(FK) -> cars.id(PK) ) |  - 
customer_id | integer | NO | foreign key ( customer_id(FK) -> customers.id(PK) ) |  - 
