# Lab - Working with Database in Python Programming

## 1. Create the following tables

### Table Name: CLIENT_MASTER

| Column Name | Data Type | Size | Attributes |
| :--- | :--- | :--- | :--- |
| CLIENTNO | Varchar | 6 | Primary Key / First letter must start with ‘C’ |
| NAME | Varchar | 20 | Not Null |
| CITY | Varchar | 15 | |
| PINCODE | Number | 8 | |
| STATE | Varchar | 15 | |
| BALDUE | Number | 10,2 | |

### Table Name: PRODUCT_MASTER

| Column Name | Data Type | Size | Attributes |
| :--- | :--- | :--- | :--- |
| PRODUCTNO | Varchar | 6 | Primary Key / First letter must start with ‘P’ |
| DESCRIPTION | Varchar | 15 | Not Null |
| PROFITPERCENT | Number | 4,2 | Not Null |
| UNITMEASURE | Varchar | 10 | Not Null |
| QTYONHAND | Number | 8 | Not Null |
| REORDERLVL | Number | 8 | Not Null |
| SELLPRICE | Number | 8,2 | Not Null, cannot be 0 |
| COSTPRICE | Number | 8,2 | Not Null, cannot be 0 |

### Table Name: SALESMAN_MASTER

| Column Name | Data Type | Size | Attributes |
| :--- | :--- | :--- | :--- |
| SALESMANNO | Varchar | 6 | Primary Key / First letter must start with ‘S’ |
| SALESMANNAME | Varchar | 20 | Not Null |
| ADDRESS1 | Varchar | 30 | Not Null |
| ADDRESS2 | Varchar | 30 | |
| CITY | Varchar | 20 | |
| PINCODE | Number | 8 | |
| STATE | Varchar | 20 | |
| SALAMT | Number | 8,2 | Not Null, cannot be 0 |
| TGTTOGET | Number | 6,2 | Not Null, cannot be 0 |
| YTDSALES | Number | 6,2 | Not Null |
| REMARKS | Varchar | 60 | |

### Table Name: SALES_ORDER

| Column Name | Data Type | Size | Attributes |
| :--- | :--- | :--- | :--- |
| ORDERNO | Varchar | 6 | Primary Key / First letter must start with ‘O’ |
| CLIENTNO | Varchar | 6 | Foreign Key references ClientNo of Client_Master table |
| ORDERDATE | Date | | Not Null |
| DELYADDR | Varchar | 25 | |
| SALESMANNO | Varchar | 6 | Foreign Key references SalesmanNo of Salesman_Master table |
| DELYTYPE | Char | 1 | |
| BILLYN | Char | 1 | |
| DELYDATE | Date | | |
| ORDERSTATUS | Varchar | 10 | |

### Table Name: SALES_ORDER_DETAILS

| Column Name | Data Type | Size | Attributes |
| :--- | :--- | :--- | :--- |
| ORDERNO | Varchar | 6 | Foreign Key references OrderNo of Sales_Order table |
| PRODUCTNO | Varchar | 6 | Foreign Key references ProductNo of Product_Master table |
| QTYORDERED | Number | 8 | |
| QTYDISP | Number | 8 | |
| PRODUCTRATE | Number | 10,2 | |

## 2. Insert the following data into their respective tables

### Data for CLIENT_MASTER
| CLIENTNO | NAME | CITY | PINCODE | STATE | BALDUE |
| :--- | :--- | :--- | :--- | :--- | :--- |
| C101 | Aman | Mumbai | 400001 | Maharashtra | 12000 |
| C102 | Ravi | Bangalore | 560001 | Karnataka | 8000 |
| C103 | Karan | Mangalore | 575001 | Karnataka | 15000 |

### Data for PRODUCT_MASTER
| PRODUCTNO | DESCRIPTION | PROFITPERCENT | UNITMEASURE | QTYONHAND | REORDERLVL | SELLPRICE | COSTPRICE |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| P01 | Laptop | 10.0 | Nos | 50 | 10 | 50000 | 45000 |
| P02 | Mouse | 15.0 | Nos | 200 | 20 | 500 | 300 |
| P03 | Keyboard | 20.0 | Nos | 150 | 15 | 800 | 600 |

### Data for SALESMAN_MASTER
| SALESMANNO | SALESMANNAME | ADDRESS1 | ADDRESS2 | CITY | PINCODE | STATE | SALAMT | TGTTOGET | YTDSALES | REMARKS |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| S01 | Raj | Address1 | Address2 | Mumbai | 400001 | Maharashtra | 10000 | 50000 | 20000 | Good |
| S02 | Vijay | Address3 | Address4 | Bangalore | 560001 | Karnataka | 12000 | 60000 | 25000 | Excellent |

### Data for SALES_ORDER
| ORDERNO | CLIENTNO | SALESMANNO | ORDERDATE | DELYADDR | DELYTYPE | BILLYN | DELYDATE | ORDERSTATUS |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| O01 | C101 | S01 | 2024-06-10 | Mumbai | F | N | 2024-06-15 | Fulfilled |
| O02 | C102 | S02 | 2024-07-12 | Bangalore | F | N | 2024-07-18 | Fulfilled |

### Data for SALES_ORDER_DETAILS
| ORDERNO | PRODUCTNO | QTYORDERED | QTYDISP | PRODUCTRATE |
| :--- | :--- | :--- | :--- | :--- |
| O01 | P01 | 1 | 1 | 50000 |
| O01 | P02 | 2 | 2 | 1000 |
| O02 | P03 | 3 | 3 | 2400 |

## 3. Generate the SQL statements to perform the following computations on table data in Python IDLE:

a. List the names of all clients having ‘a’ as the second letter in their names.
b. List the clients who stay in a city whose first letter is ‘M’.
c. List all clients who stay in ‘Bangalore’ or ‘Mangalore’.
d. List all clients whose BalDue is greater than value 10000.
e. List all information from the Sales_order table for order placed in the month of June.
f. List the Order No & day on which clients placed their order.
g. List the names, city and state of clients who are not in the state of ‘Maharashtra’.

## 4. Exercises on Using Having, Group By and Joins in Python IDLE:

a. Printing the description and total quantity sold for each product.
b. Calculating the average quantity sold for each client that has a maximum order value of 15000.00.
