## Create Table
```sql
CREATE TABLE EmployeeSales (
    EmployeeID INT,
    Region VARCHAR(50),
    Category VARCHAR(50),
    Quarter VARCHAR(10),
    SalesAmount DECIMAL(10,2)
);
```

## Insert Values
```sql
INSERT INTO EmployeeSales (EmployeeID, Region, Category, Quarter, SalesAmount)
VALUES
    (101, 'North', 'Electronics', 'Q1', 1200.00),
    (101, 'North', 'Electronics', 'Q2', 1500.00),
    (102, 'North', 'Clothing', 'Q1', 800.00),
    (102, 'North', 'Clothing', 'Q2', 950.00),
    (103, 'South', 'Electronics', 'Q1', 1000.00),
    (103, 'South', 'Clothing', 'Q1', 1200.00),
    (104, 'East', 'Electronics', 'Q2', 1150.00),
    (104, 'East', 'Clothing', 'Q2', 500.00),
    (105, 'West', 'Electronics', 'Q1', 1900.00),
    (105, 'West', 'Clothing', 'Q1', 1100.00),
    (105, 'West', 'Electronics', 'Q2', 2100.00),
    (105, 'West', 'Clothing', 'Q2', 1300.00);
```

### Generated Table:

| EmployeeID | Region | Category    | Quarter | SalesAmount |
|------------|--------|-------------|---------|-------------|
| 101        | North  | Electronics | Q1      | 1200.00     |
| 101        | North  | Electronics | Q2      | 1500.00     |
| 102        | North  | Clothing    | Q1      | 800.00      |
| 102        | North  | Clothing    | Q2      | 950.00      |
| 103        | South  | Electronics | Q1      | 1000.00     |
| 103        | South  | Clothing    | Q1      | 1200.00     |
| 104        | East   | Electronics | Q2      | 1150.00     |
| 104        | East   | Clothing    | Q2      | 500.00      |
| 105        | West   | Electronics | Q1      | 1900.00     |
| 105        | West   | Clothing    | Q1      | 1100.00     |
| 105        | West   | Electronics | Q2      | 2100.00     |
| 105        | West   | Clothing    | Q2      | 1300.00     |
