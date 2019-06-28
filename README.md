Car rent service
================

	Database consists of 3 tables:
1. cars
2. customers
3. orders


Table "cars":
--------------

Column | Type | Nullable | Constraints 
--- | --- | --- | --- 
id | integer |  NO | primary key
name | character varying |  NO |  - 
cost | integer |  NO |  - 
storage | character varying |  NO |  - 
amount | integer | NO | - 



Table "customers":
--------------

Column | Type | Nullable |  Constraints
--- | --- | --- | --- 
id | integer |  NO |  primary key 
name | character varying |  NO |  - 
area | character varying |  NO |  -
discount | integer |  NO |  -



Table "orders":
--------------

Column | Type | Nullable | Constraints
--- | --- | --- | ---
order_id | integer |  NO |  primary key 
date | date |  NO |  - 
amount | integer |  NO |  -
car_id | integer |  NO |  foreign key ( car_id(FK) -> car.id(PK) )
customer_id | integer | NO | foreign key ( customer_id(FK) -> customer.id(PK) )
