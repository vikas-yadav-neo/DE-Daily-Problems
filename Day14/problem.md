# 📝 Problem 1: PySpark – Detect Consecutive Days Without Sales

### **Problem Statement**

You have a PySpark DataFrame with daily sales data. Some days may have **zero sales**. Write a PySpark program to **find all periods where a product had at least 2 consecutive days of zero sales**.

### **Sample Input** (`daily_sales`)

| product | sale\_date | sales |
| ------- | ---------- | ----- |
| Laptop  | 2025-01-01 | 100   |
| Laptop  | 2025-01-02 | 0     |
| Laptop  | 2025-01-03 | 0     |
| Laptop  | 2025-01-04 | 50    |
| Phone   | 2025-01-01 | 200   |
| Phone   | 2025-01-02 | 0     |
| Phone   | 2025-01-03 | 300   |

### **Expected Output**

| product | start\_date | end\_date  | zero\_days |
| ------- | ----------- | ---------- | ---------- |
| Laptop  | 2025-01-02  | 2025-01-03 | 2          |

*(Laptop had 2 consecutive zero-sales days, Phone had only 1 so it’s excluded)*

---

# 📝 Problem 2: SQL – Find Employees with Overlapping Project Assignments

### **Problem Statement**

You have a SQL table `employee_projects(emp_id, project_id, start_date, end_date)` that records employee assignments to projects. Write a SQL query to **find employees who were assigned to multiple projects that overlapped in time**.

### **Sample Input** (`employee_projects`)

| emp\_id | project\_id | start\_date | end\_date  |
| ------- | ----------- | ----------- | ---------- |
| 1       | P1          | 2025-01-01  | 2025-02-15 |
| 1       | P2          | 2025-02-01  | 2025-03-10 |
| 2       | P3          | 2025-01-05  | 2025-01-20 |
| 2       | P4          | 2025-02-01  | 2025-02-28 |
| 3       | P5          | 2025-01-10  | 2025-01-25 |

### **Expected Output**

| emp\_id | project1 | project2 |
| ------- | -------- | -------- |
| 1       | P1       | P2       |

---