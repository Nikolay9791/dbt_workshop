# dbt_workshop


```sql
select 1 
```


## Создать таблицы и схемы

```sql
create schema if not exists jaffle_shop;
create schema if not exists stripe;

create table jaffle_shop.customers(
    id integer,
    first_name varchar(50),
    last_name varchar(50)
);

create table jaffle_shop.orders(
    id integer,
    user_id integer,
    order_date date,
    status varchar(50)
);

create table stripe.payment(
    id integer,
    orderid integer,
    paymentmethod varchar(50),
    status varchar(50),
    amount integer,
    created date
);
```


## Вставить данные

В таблицу `jaffle_shop.customers`

```sql
INSERT INTO jaffle_shop.customers (ID, FIRST_NAME, LAST_NAME) VALUES (1, 'Michael', 'P.');
INSERT INTO jaffle_shop.customers (ID, FIRST_NAME, LAST_NAME) VALUES (2, 'Shawn', 'M.');
INSERT INTO jaffle_shop.customers (ID, FIRST_NAME, LAST_NAME) VALUES (3, 'Kathleen', 'P.');
INSERT INTO jaffle_shop.customers (ID, FIRST_NAME, LAST_NAME) VALUES (4, 'Jimmy', 'C.');
INSERT INTO jaffle_shop.customers (ID, FIRST_NAME, LAST_NAME) VALUES (5, 'Katherine', 'R.');
INSERT INTO jaffle_shop.customers (ID, FIRST_NAME, LAST_NAME) VALUES (6, 'Sarah', 'R.');
INSERT INTO jaffle_shop.customers (ID, FIRST_NAME, LAST_NAME) VALUES (7, 'Martin', 'M.');
INSERT INTO jaffle_shop.customers (ID, FIRST_NAME, LAST_NAME) VALUES (8, 'Frank', 'R.');
INSERT INTO jaffle_shop.customers (ID, FIRST_NAME, LAST_NAME) VALUES (9, 'Jennifer', 'F.');
INSERT INTO jaffle_shop.customers (ID, FIRST_NAME, LAST_NAME) VALUES (10, 'Henry', 'W.');
INSERT INTO jaffle_shop.customers (ID, FIRST_NAME, LAST_NAME) VALUES (11, 'Fred', 'S.');
INSERT INTO jaffle_shop.customers (ID, FIRST_NAME, LAST_NAME) VALUES (12, 'Amy', 'D.');
INSERT INTO jaffle_shop.customers (ID, FIRST_NAME, LAST_NAME) VALUES (13, 'Kathleen', 'M.');
INSERT INTO jaffle_shop.customers (ID, FIRST_NAME, LAST_NAME) VALUES (14, 'Steve', 'F.');
INSERT INTO jaffle_shop.customers (ID, FIRST_NAME, LAST_NAME) VALUES (15, 'Teresa', 'H.');
INSERT INTO jaffle_shop.customers (ID, FIRST_NAME, LAST_NAME) VALUES (16, 'Amanda', 'H.');
INSERT INTO jaffle_shop.customers (ID, FIRST_NAME, LAST_NAME) VALUES (17, 'Kimberly', 'R.');
INSERT INTO jaffle_shop.customers (ID, FIRST_NAME, LAST_NAME) VALUES (18, 'Johnny', 'K.');
INSERT INTO jaffle_shop.customers (ID, FIRST_NAME, LAST_NAME) VALUES (19, 'Virginia', 'F.');
INSERT INTO jaffle_shop.customers (ID, FIRST_NAME, LAST_NAME) VALUES (20, 'Anna', 'A.');
INSERT INTO jaffle_shop.customers (ID, FIRST_NAME, LAST_NAME) VALUES (21, 'Willie', 'H.');
INSERT INTO jaffle_shop.customers (ID, FIRST_NAME, LAST_NAME) VALUES (22, 'Sean', 'H.');
INSERT INTO jaffle_shop.customers (ID, FIRST_NAME, LAST_NAME) VALUES (23, 'Mildred', 'A.');
INSERT INTO jaffle_shop.customers (ID, FIRST_NAME, LAST_NAME) VALUES (24, 'David', 'G.');
INSERT INTO jaffle_shop.customers (ID, FIRST_NAME, LAST_NAME) VALUES (25, 'Victor', 'H.');
INSERT INTO jaffle_shop.customers (ID, FIRST_NAME, LAST_NAME) VALUES (26, 'Aaron', 'R.');
INSERT INTO jaffle_shop.customers (ID, FIRST_NAME, LAST_NAME) VALUES (27, 'Benjamin', 'B.');
INSERT INTO jaffle_shop.customers (ID, FIRST_NAME, LAST_NAME) VALUES (28, 'Lisa', 'W.');
INSERT INTO jaffle_shop.customers (ID, FIRST_NAME, LAST_NAME) VALUES (29, 'Benjamin', 'K.');
INSERT INTO jaffle_shop.customers (ID, FIRST_NAME, LAST_NAME) VALUES (30, 'Christina', 'W.');
INSERT INTO jaffle_shop.customers (ID, FIRST_NAME, LAST_NAME) VALUES (31, 'Jane', 'G.');
INSERT INTO jaffle_shop.customers (ID, FIRST_NAME, LAST_NAME) VALUES (32, 'Thomas', 'O.');
INSERT INTO jaffle_shop.customers (ID, FIRST_NAME, LAST_NAME) VALUES (33, 'Katherine', 'M.');
INSERT INTO jaffle_shop.customers (ID, FIRST_NAME, LAST_NAME) VALUES (34, 'Jennifer', 'S.');
INSERT INTO jaffle_shop.customers (ID, FIRST_NAME, LAST_NAME) VALUES (35, 'Sara', 'T.');
INSERT INTO jaffle_shop.customers (ID, FIRST_NAME, LAST_NAME) VALUES (36, 'Harold', 'O.');
INSERT INTO jaffle_shop.customers (ID, FIRST_NAME, LAST_NAME) VALUES (37, 'Shirley', 'J.');
INSERT INTO jaffle_shop.customers (ID, FIRST_NAME, LAST_NAME) VALUES (38, 'Dennis', 'J.');
INSERT INTO jaffle_shop.customers (ID, FIRST_NAME, LAST_NAME) VALUES (39, 'Louise', 'W.');
INSERT INTO jaffle_shop.customers (ID, FIRST_NAME, LAST_NAME) VALUES (40, 'Maria', 'A.');
INSERT INTO jaffle_shop.customers (ID, FIRST_NAME, LAST_NAME) VALUES (41, 'Gloria', 'C.');
INSERT INTO jaffle_shop.customers (ID, FIRST_NAME, LAST_NAME) VALUES (42, 'Diana', 'S.');
INSERT INTO jaffle_shop.customers (ID, FIRST_NAME, LAST_NAME) VALUES (43, 'Kelly', 'N.');
INSERT INTO jaffle_shop.customers (ID, FIRST_NAME, LAST_NAME) VALUES (44, 'Jane', 'R.');
INSERT INTO jaffle_shop.customers (ID, FIRST_NAME, LAST_NAME) VALUES (45, 'Scott', 'B.');
INSERT INTO jaffle_shop.customers (ID, FIRST_NAME, LAST_NAME) VALUES (46, 'Norma', 'C.');
INSERT INTO jaffle_shop.customers (ID, FIRST_NAME, LAST_NAME) VALUES (47, 'Marie', 'P.');
INSERT INTO jaffle_shop.customers (ID, FIRST_NAME, LAST_NAME) VALUES (48, 'Lillian', 'C.');
INSERT INTO jaffle_shop.customers (ID, FIRST_NAME, LAST_NAME) VALUES (49, 'Judy', 'N.');
INSERT INTO jaffle_shop.customers (ID, FIRST_NAME, LAST_NAME) VALUES (50, 'Billy', 'L.');
INSERT INTO jaffle_shop.customers (ID, FIRST_NAME, LAST_NAME) VALUES (51, 'Howard', 'R.');
INSERT INTO jaffle_shop.customers (ID, FIRST_NAME, LAST_NAME) VALUES (52, 'Laura', 'F.');
INSERT INTO jaffle_shop.customers (ID, FIRST_NAME, LAST_NAME) VALUES (53, 'Anne', 'B.');
INSERT INTO jaffle_shop.customers (ID, FIRST_NAME, LAST_NAME) VALUES (54, 'Rose', 'M.');
INSERT INTO jaffle_shop.customers (ID, FIRST_NAME, LAST_NAME) VALUES (55, 'Nicholas', 'R.');
INSERT INTO jaffle_shop.customers (ID, FIRST_NAME, LAST_NAME) VALUES (56, 'Joshua', 'K.');
INSERT INTO jaffle_shop.customers (ID, FIRST_NAME, LAST_NAME) VALUES (57, 'Paul', 'W.');
INSERT INTO jaffle_shop.customers (ID, FIRST_NAME, LAST_NAME) VALUES (58, 'Kathryn', 'K.');
INSERT INTO jaffle_shop.customers (ID, FIRST_NAME, LAST_NAME) VALUES (59, 'Adam', 'A.');
INSERT INTO jaffle_shop.customers (ID, FIRST_NAME, LAST_NAME) VALUES (60, 'Norma', 'W.');
INSERT INTO jaffle_shop.customers (ID, FIRST_NAME, LAST_NAME) VALUES (61, 'Timothy', 'R.');
INSERT INTO jaffle_shop.customers (ID, FIRST_NAME, LAST_NAME) VALUES (62, 'Elizabeth', 'P.');
INSERT INTO jaffle_shop.customers (ID, FIRST_NAME, LAST_NAME) VALUES (63, 'Edward', 'G.');
INSERT INTO jaffle_shop.customers (ID, FIRST_NAME, LAST_NAME) VALUES (64, 'David', 'C.');
INSERT INTO jaffle_shop.customers (ID, FIRST_NAME, LAST_NAME) VALUES (65, 'Brenda', 'W.');
INSERT INTO jaffle_shop.customers (ID, FIRST_NAME, LAST_NAME) VALUES (66, 'Adam', 'W.');
INSERT INTO jaffle_shop.customers (ID, FIRST_NAME, LAST_NAME) VALUES (67, 'Michael', 'H.');
INSERT INTO jaffle_shop.customers (ID, FIRST_NAME, LAST_NAME) VALUES (68, 'Jesse', 'E.');
INSERT INTO jaffle_shop.customers (ID, FIRST_NAME, LAST_NAME) VALUES (69, 'Janet', 'P.');
INSERT INTO jaffle_shop.customers (ID, FIRST_NAME, LAST_NAME) VALUES (70, 'Helen', 'F.');
INSERT INTO jaffle_shop.customers (ID, FIRST_NAME, LAST_NAME) VALUES (71, 'Gerald', 'C.');
INSERT INTO jaffle_shop.customers (ID, FIRST_NAME, LAST_NAME) VALUES (72, 'Kathryn', 'O.');
INSERT INTO jaffle_shop.customers (ID, FIRST_NAME, LAST_NAME) VALUES (73, 'Alan', 'B.');
INSERT INTO jaffle_shop.customers (ID, FIRST_NAME, LAST_NAME) VALUES (74, 'Harry', 'A.');
INSERT INTO jaffle_shop.customers (ID, FIRST_NAME, LAST_NAME) VALUES (75, 'Andrea', 'H.');
INSERT INTO jaffle_shop.customers (ID, FIRST_NAME, LAST_NAME) VALUES (76, 'Barbara', 'W.');
INSERT INTO jaffle_shop.customers (ID, FIRST_NAME, LAST_NAME) VALUES (77, 'Anne', 'W.');
INSERT INTO jaffle_shop.customers (ID, FIRST_NAME, LAST_NAME) VALUES (78, 'Harry', 'H.');
INSERT INTO jaffle_shop.customers (ID, FIRST_NAME, LAST_NAME) VALUES (79, 'Jack', 'R.');
INSERT INTO jaffle_shop.customers (ID, FIRST_NAME, LAST_NAME) VALUES (80, 'Phillip', 'H.');
INSERT INTO jaffle_shop.customers (ID, FIRST_NAME, LAST_NAME) VALUES (81, 'Shirley', 'H.');
INSERT INTO jaffle_shop.customers (ID, FIRST_NAME, LAST_NAME) VALUES (82, 'Arthur', 'D.');
INSERT INTO jaffle_shop.customers (ID, FIRST_NAME, LAST_NAME) VALUES (83, 'Virginia', 'R.');
INSERT INTO jaffle_shop.customers (ID, FIRST_NAME, LAST_NAME) VALUES (84, 'Christina', 'R.');
INSERT INTO jaffle_shop.customers (ID, FIRST_NAME, LAST_NAME) VALUES (85, 'Theresa', 'M.');
INSERT INTO jaffle_shop.customers (ID, FIRST_NAME, LAST_NAME) VALUES (86, 'Jason', 'C.');
INSERT INTO jaffle_shop.customers (ID, FIRST_NAME, LAST_NAME) VALUES (87, 'Phillip', 'B.');
INSERT INTO jaffle_shop.customers (ID, FIRST_NAME, LAST_NAME) VALUES (88, 'Adam', 'T.');
INSERT INTO jaffle_shop.customers (ID, FIRST_NAME, LAST_NAME) VALUES (89, 'Margaret', 'J.');
INSERT INTO jaffle_shop.customers (ID, FIRST_NAME, LAST_NAME) VALUES (90, 'Paul', 'P.');
INSERT INTO jaffle_shop.customers (ID, FIRST_NAME, LAST_NAME) VALUES (91, 'Todd', 'W.');
INSERT INTO jaffle_shop.customers (ID, FIRST_NAME, LAST_NAME) VALUES (92, 'Willie', 'O.');
INSERT INTO jaffle_shop.customers (ID, FIRST_NAME, LAST_NAME) VALUES (93, 'Frances', 'R.');
INSERT INTO jaffle_shop.customers (ID, FIRST_NAME, LAST_NAME) VALUES (94, 'Gregory', 'H.');
INSERT INTO jaffle_shop.customers (ID, FIRST_NAME, LAST_NAME) VALUES (95, 'Lisa', 'P.');
INSERT INTO jaffle_shop.customers (ID, FIRST_NAME, LAST_NAME) VALUES (96, 'Jacqueline', 'A.');
INSERT INTO jaffle_shop.customers (ID, FIRST_NAME, LAST_NAME) VALUES (97, 'Shirley', 'D.');
INSERT INTO jaffle_shop.customers (ID, FIRST_NAME, LAST_NAME) VALUES (98, 'Nicole', 'M.');
INSERT INTO jaffle_shop.customers (ID, FIRST_NAME, LAST_NAME) VALUES (99, 'Mary', 'G.');
INSERT INTO jaffle_shop.customers (ID, FIRST_NAME, LAST_NAME) VALUES (100, 'Jean', 'M.');

```

В таблицу `jaffle_shop.orders`

```sql
INSERT INTO jaffle_shop.orders (id, user_id, order_date, status) VALUES
(1, 1, '2018-01-01', 'returned'),
(2, 3, '2018-01-02', 'completed'),
(3, 94, '2018-01-04', 'completed'),
(4, 50, '2018-01-05', 'completed'),
(5, 64, '2018-01-05', 'completed'),
(6, 54, '2018-01-07', 'completed'),
(7, 88, '2018-01-09', 'completed'),
(8, 2, '2018-01-11', 'returned'),
(9, 53, '2018-01-12', 'completed'),
(10, 7, '2018-01-14', 'completed'),
(11, 99, '2018-01-14', 'completed'),
(12, 59, '2018-01-15', 'completed'),
(13, 84, '2018-01-17', 'completed'),
(14, 40, '2018-01-17', 'returned'),
(15, 25, '2018-01-17', 'completed'),
(16, 39, '2018-01-18', 'completed'),
(17, 71, '2018-01-18', 'completed'),
(18, 64, '2018-01-20', 'returned'),
(19, 54, '2018-01-22', 'completed'),
(20, 20, '2018-01-23', 'completed'),
(21, 71, '2018-01-23', 'completed'),
(22, 86, '2018-01-24', 'completed'),
(23, 22, '2018-01-26', 'return_pending'),
(24, 3, '2018-01-27', 'completed'),
(25, 51, '2018-01-28', 'completed'),
(26, 32, '2018-01-28', 'completed'),
(27, 94, '2018-01-29', 'completed'),
(28, 8, '2018-01-29', 'completed'),
(29, 57, '2018-01-31', 'completed'),
(30, 69, '2018-02-02', 'completed'),
(31, 16, '2018-02-02', 'completed'),
(32, 28, '2018-02-04', 'completed'),
(33, 42, '2018-02-04', 'completed'),
(34, 38, '2018-02-06', 'completed'),
(35, 80, '2018-02-08', 'completed'),
(36, 85, '2018-02-10', 'completed'),
(37, 1, '2018-02-10', 'completed'),
(38, 51, '2018-02-10', 'completed'),
(39, 26, '2018-02-11', 'completed'),
(40, 33, '2018-02-13', 'completed'),
(41, 99, '2018-02-14', 'completed'),
(42, 92, '2018-02-16', 'completed'),
(43, 31, '2018-02-17', 'completed'),
(44, 66, '2018-02-17', 'completed'),
(45, 22, '2018-02-17', 'completed'),
(46, 6, '2018-02-19', 'completed'),
(47, 50, '2018-02-20', 'completed'),
(48, 27, '2018-02-21', 'completed'),
(49, 35, '2018-02-21', 'completed'),
(50, 51, '2018-02-23', 'completed'),
(51, 71, '2018-02-24', 'completed'),
(52, 54, '2018-02-25', 'return_pending'),
(53, 34, '2018-02-26', 'completed'),
(54, 54, '2018-02-26', 'completed'),
(55, 18, '2018-02-27', 'completed'),
(56, 79, '2018-02-28', 'completed'),
(57, 93, '2018-03-01', 'completed'),
(58, 22, '2018-03-01', 'completed'),
(59, 30, '2018-03-02', 'completed'),
(60, 12, '2018-03-03', 'completed'),
(61, 63, '2018-03-03', 'completed'),
(62, 57, '2018-03-05', 'completed'),
(63, 70, '2018-03-06', 'completed'),
(64, 13, '2018-03-07', 'completed'),
(65, 26, '2018-03-08', 'completed'),
(66, 36, '2018-03-10', 'completed'),
(67, 79, '2018-03-11', 'completed'),
(68, 53, '2018-03-11', 'completed'),
(69, 3, '2018-03-11', 'completed'),
(70, 8, '2018-03-12', 'completed'),
(71, 42, '2018-03-12', 'shipped'),
(72, 30, '2018-03-14', 'shipped'),
(73, 19, '2018-03-16', 'completed'),
(74, 9, '2018-03-17', 'shipped'),
(75, 69, '2018-03-18', 'completed'),
(76, 25, '2018-03-20', 'completed'),
(77, 35, '2018-03-21', 'shipped'),
(78, 90, '2018-03-23', 'shipped'),
(79, 52, '2018-03-23', 'shipped'),
(80, 11, '2018-03-23', 'shipped'),
(81, 76, '2018-03-23', 'shipped'),
(82, 46, '2018-03-24', 'shipped'),
(83, 54, '2018-03-24', 'shipped'),
(84, 70, '2018-03-26', 'placed'),
(85, 47, '2018-03-26', 'shipped'),
(86, 68, '2018-03-26', 'placed'),
(87, 46, '2018-03-27', 'placed'),
(88, 91, '2018-03-27', 'shipped'),
(89, 21, '2018-03-28', 'placed'),
(90, 66, '2018-03-30', 'shipped'),
(91, 47, '2018-03-31', 'placed'),
(92, 84, '2018-04-02', 'placed'),
(93, 66, '2018-04-03', 'placed'),
(94, 63, '2018-04-03', 'placed'),
(95, 27, '2018-04-04', 'placed'),
(96, 90, '2018-04-06', 'placed'),
(97, 89, '2018-04-07', 'placed'),
(98, 41, '2018-04-07', 'placed'),
(99, 85, '2018-04-09', 'placed');
```

В таблицу `stripe.payment`

```sql
INSERT INTO stripe.payment (id, orderid, paymentmethod, status, amount, created) VALUES
(69, 56, 'credit_card', 'success', 400, '2018-02-28'),
(70, 57, 'bank_transfer', 'success', 200, '2018-03-01'),
(71, 58, 'coupon', 'fail', 1800, '2018-03-01'),
(72, 58, 'coupon', 'success', 1800, '2018-03-01'),
(73, 58, 'gift_card', 'success', 600, '2018-03-01'),
(74, 59, 'gift_card', 'success', 2800, '2018-03-02'),
(75, 60, 'credit_card', 'success', 400, '2018-03-03'),
(76, 61, 'bank_transfer', 'success', 1600, '2018-03-03'),
(77, 62, 'gift_card', 'success', 1400, '2018-03-05'),
(78, 63, 'credit_card', 'success', 2900, '2018-03-06'),
(79, 64, 'bank_transfer', 'success', 2600, '2018-03-07'),
(80, 65, 'credit_card', 'success', 0, '2018-03-08'),
(81, 66, 'credit_card', 'success', 2800, '2018-03-10'),
(82, 67, 'bank_transfer', 'success', 400, '2018-03-11'),
(83, 67, 'credit_card', 'success', 1900, '2018-03-11'),
(84, 68, 'credit_card', 'success', 1600, '2018-03-11'),
(85, 69, 'credit_card', 'success', 1900, '2018-03-11'),
(86, 70, 'credit_card', 'success', 2600, '2018-03-12'),
(87, 71, 'credit_card', 'success', 500, '2018-03-12'),
(88, 72, 'credit_card', 'success', 2900, '2018-03-14'),
(89, 73, 'bank_transfer', 'success', 300, '2018-03-16'),
(90, 74, 'credit_card', 'success', 3000, '2018-03-17'),
(91, 75, 'credit_card', 'success', 1900, '2018-03-18'),
(92, 76, 'coupon', 'success', 200, '2018-03-20'),
(93, 77, 'credit_card', 'success', 0, '2018-03-21'),
(94, 77, 'bank_transfer', 'success', 1900, '2018-03-21'),
(95, 78, 'bank_transfer', 'success', 2600, '2018-03-23'),
(96, 79, 'credit_card', 'success', 1800, '2018-03-23'),
(97, 79, 'credit_card', 'success', 900, '2018-03-23'),
(98, 80, 'gift_card', 'success', 300, '2018-03-23'),
(99, 81, 'coupon', 'success', 200, '2018-03-23'),
(100, 82, 'credit_card', 'success', 800, '2018-03-24'),
(101, 83, 'credit_card', 'success', 100, '2018-03-24'),
(102, 84, 'bank_transfer', 'success', 2500, '2018-03-26'),
(103, 85, 'bank_transfer', 'success', 1700, '2018-03-26'),
(104, 86, 'coupon', 'success', 2300, '2018-03-26'),
(105, 87, 'gift_card', 'success', 3000, '2018-03-27'),
(106, 87, 'credit_card', 'success', 2600, '2018-03-27'),
(107, 88, 'credit_card', 'success', 2900, '2018-03-27'),
(108, 89, 'bank_transfer', 'success', 2200, '2018-03-28'),
(109, 90, 'bank_transfer', 'success', 200, '2018-03-30'),
(110, 91, 'credit_card', 'success', 1900, '2018-03-31'),
(111, 92, 'bank_transfer', 'success', 1500, '2018-04-02'),
(112, 92, 'coupon', 'success', 200, '2018-04-02'),
(113, 93, 'gift_card', 'success', 2600, '2018-04-03'),
(114, 94, 'gift_card', 'fail', 700, '2018-04-03'),
(115, 94, 'coupon', 'success', 700, '2018-04-03'),
(116, 95, 'coupon', 'success', 2400, '2018-04-04');


INSERT INTO stripe.payment (ID, ORDERID, PAYMENTMETHOD, STATUS, AMOUNT, CREATED) VALUES
(1, 1, 'credit_card', 'success', 1000, '2018-01-01'),
(2, 2, 'credit_card', 'success', 2000, '2018-01-02'),
(3, 3, 'coupon', 'success', 100, '2018-01-04'),
(4, 4, 'coupon', 'success', 2500, '2018-01-05'),
(5, 5, 'bank_transfer', 'fail', 1700, '2018-01-05'),
(6, 5, 'bank_transfer', 'success', 1700, '2018-01-05'),
(7, 6, 'credit_card', 'success', 600, '2018-01-07'),
(8, 7, 'credit_card', 'success', 1600, '2018-01-09'),
(9, 8, 'credit_card', 'success', 2300, '2018-01-11'),
(10, 9, 'gift_card', 'success', 2300, '2018-01-12'),
(11, 9, 'bank_transfer', 'success', 0, '2018-01-12'),
(12, 10, 'bank_transfer', 'success', 2600, '2018-01-14'),
(13, 11, 'credit_card', 'success', 2700, '2018-01-14'),
(14, 12, 'credit_card', 'success', 100, '2018-01-15'),
(15, 13, 'credit_card', 'fail', 500, '2018-01-17'),
(16, 13, 'bank_transfer', 'success', 500, '2018-01-17'),
(17, 13, 'bank_transfer', 'success', 1400, '2018-01-17'),
(18, 14, 'bank_transfer', 'success', 300, '2018-01-17'),
(19, 15, 'coupon', 'success', 2200, '2018-01-17'),
(20, 16, 'credit_card', 'success', 1000, '2018-01-18'),
(21, 17, 'bank_transfer', 'success', 200, '2018-01-18'),
(22, 18, 'credit_card', 'success', 500, '2018-01-20'),
(23, 18, 'credit_card', 'success', 800, '2018-01-20'),
(24, 19, 'gift_card', 'success', 600, '2018-01-22'),
(25, 20, 'bank_transfer', 'success', 1500, '2018-01-23'),
(26, 21, 'credit_card', 'success', 1200, '2018-01-23'),
(27, 22, 'bank_transfer', 'success', 800, '2018-01-24'),
(28, 23, 'gift_card', 'fail', 2300, '2018-01-26'),
(29, 23, 'credit_card', 'success', 2300, '2018-01-26'),
(30, 24, 'coupon', 'success', 2600, '2018-01-27'),
(31, 25, 'bank_transfer', 'success', 2000, '2018-01-28'),
(32, 25, 'credit_card', 'success', 2200, '2018-01-28'),
(33, 25, 'coupon', 'success', 1600, '2018-01-28'),
(34, 26, 'credit_card', 'success', 3000, '2018-01-28'),
(35, 27, 'credit_card', 'success', 2300, '2018-01-29'),
(36, 28, 'bank_transfer', 'success', 1900, '2018-01-29'),
(37, 29, 'bank_transfer', 'success', 1200, '2018-01-31'),
(38, 30, 'credit_card', 'success', 1300, '2018-02-02'),
(39, 31, 'credit_card', 'success', 1200, '2018-02-02'),
(40, 32, 'credit_card', 'success', 300, '2018-02-04'),
(41, 33, 'credit_card', 'success', 2200, '2018-02-04'),
(42, 34, 'bank_transfer', 'success', 1500, '2018-02-06'),
(43, 35, 'credit_card', 'success', 2900, '2018-02-08'),
(44, 36, 'bank_transfer', 'success', 900, '2018-02-10'),
(45, 37, 'credit_card', 'success', 2300, '2018-02-10'),
(46, 38, 'credit_card', 'fail', 1500, '2018-02-10'),
(47, 38, 'credit_card', 'success', 1500, '2018-02-10'),
(48, 39, 'bank_transfer', 'success', 800, '2018-02-11'),
(49, 40, 'credit_card', 'success', 1400, '2018-02-13'),
(50, 41, 'credit_card', 'success', 1700, '2018-02-14'),
(51, 42, 'coupon', 'success', 1700, '2018-02-16'),
(52, 43, 'gift_card', 'success', 1800, '2018-02-17'),
(53, 44, 'gift_card', 'success', 1100, '2018-02-17'),
(54, 45, 'bank_transfer', 'success', 500, '2018-02-17'),
(55, 46, 'bank_transfer', 'success', 800, '2018-02-19'),
(56, 47, 'credit_card', 'success', 2200, '2018-02-20'),
(57, 48, 'bank_transfer', 'success', 300, '2018-02-21'),
(58, 49, 'bank_transfer', 'fail', 600, '2018-02-21'),
(59, 49, 'credit_card', 'success', 600, '2018-02-21'),
(60, 49, 'credit_card', 'success', 900, '2018-02-21'),
(61, 50, 'credit_card', 'success', 2600, '2018-02-23'),
(62, 51, 'credit_card', 'success', 2900, '2018-02-24'),
(63, 51, 'credit_card', 'success', 100, '2018-02-24'),
(64, 52, 'bank_transfer', 'success', 1500, '2018-02-25');

```
hi