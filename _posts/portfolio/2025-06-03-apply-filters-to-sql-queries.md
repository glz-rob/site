---
layout: post
title:  "Apply filters to SQL queries"
date:   2025-06-03
categories: portfolio security
---

# Apply filters to SQL queries

## Project Description

This organization is working to improve the system's security. My job is to ensure that teh system is safe, investigating potential security issues, and update computers as needed. The following steps show how I used SQL to perform security-related tasks.

## Scenario

You are a security professional at a large organization. Part of your job is to investigate security issues to help keep the system secure. You recently discovered some potential security issues that involve login attempts and employee machines.

Your task is to examine the organization’s data in their employees and log_in_attempts tables. You’ll need to use SQL filters to retrieve records from different datasets and investigate the potential security issues.

Note: This scenario involves the same queries as the ones the Filter with AND, OR, and NOT lab. You can revisit the lab to get screenshots to include in your portfolio document. If you choose, it's also possible to complete this activity without revisiting the lab by typing your queries in the template

### Table formats

This document describes how the tables used for this portfolio activity are organized. The organization database contains the following two tables:

- log_in_attempts

- employees

#### log_in_attempts

The log_in_attempts table has the following columns:

- event_id: The identification number assigned to each login event

- username: The username of the employee

- login_date: The date the login attempt was recorded

- login_time: The time the login attempt was recorded

- country: The country where the login attempt occurred

- ip_address: The IP address of that employee’s machine

- success: The success of the login attempt; FALSE indicates a failed attempt

#### employees

The employees table has the following columns:

- employee_id: The identification number assigned to each employee

- device_id: The identification number assigned to each device used by the employee

- username: The username of the employee

- department: The department the employee is in

- office: The office the employee is located in

## Retrieve after hours failed login attempts

*You recently discovered a potential security incident that occurred after business hours. To investigate this, you need to query the `log_in_attempts` table and review after hours login activity. Use filters in SQL to create a query that identifies all failed login attempts that occurred after `18:00`. (The time of the login attempt is found in the `login_time` column. The `success` column contains a value of `0` when a login attempt failed; you can use either a value of `0` or `FALSE` in your query to identify failed login attempts.)*

```SQL
SELECT *
FROM log_in_attempts
WHERE login_time > '18:00' AND success = FALSE;
```

This query will retrieve all the records from the `log_in_attempts` table that have a `login_time` value greater than `18:00` and with that their `success` column value is `FALSE`.

## Retrieve login attempts on specific dates

*A suspicious event occurred on `2022-05-09`. To investigate this event, you want to review all login attempts which occurred on this day and the day before. Use filters in SQL to create a query that identifies all login attempts that occurred on `2022-05-09` or `2022-05-08`. (The date of the login attempt is found in the `login_date` column.)*

```SQL
SELECT *
FROM log_in_attempts
WHERE login_date = '2022-05-08' OR login_date = '2022-05-09';
```

This query will retrieve all the records from the `log_in_attempts` table that have a `login_date` equals to `2022-05-08` or `2022-05-09`.

## Retrieve login attempts outside of Mexico

*There’s been suspicious activity with login attempts, but the team has determined that this activity didn't originate in Mexico. Now, you need to investigate login attempts that occurred outside of Mexico. Use filters in SQL to create a query that identifies all login attempts that occurred outside of Mexico. (When referring to Mexico, the `country` column contains values of both `MEX` and `MEXICO`, and you need to use the `LIKE` keyword with `%` to make sure your query reflects this.)*

```SQL
SELECT *
FROM log_in_attempts
WHERE NOT country LIKE 'MEX%';
```

This query will select all the records from `log_in_attempts` that don't match the pattern `'MEX%'`, which indicates all the strings that start with `'MEX'`.

## Retrieve employees in Marketing

*Your team wants to perform security updates on specific employee machines in the Marketing department. You’re responsible for getting information on these employee machines and will need to query the employees table. Use filters in SQL to create a query that identifies all employees in the Marketing department for all offices in the East building.

(The department of the employee is found in the `department` column, which contains values that include `Marketing`. The office is found in the office column. Some examples of values in this column are `East-170`, `East-320`, and `North-434`. You’ll need to use the `LIKE` keyword with `%` to filter for the East building.)*


```SQL
SELECT *
FROM employees
WHERE department = 'Marketing' AND office LIKE 'East%';
```

This query will return all the records from `emplyees` whose `department` matches `'Marketing'` and `office` start with the string `'East'`.

## Retrieve employees in Finance or Sales

*Your team now needs to perform a different security update on machines for employees in the Sales and Finance departments. Use filters in SQL to create a query that identifies all employees in the Sales or Finance departments. (The department of the employee is found in the `department` column, which contains values that include `Sales` and `Finance`.)*

```SQL
SELECT *
FROM employees
WHERE department = 'Sales' OR department = 'Finance';
```

This query will return all the records from `employees` whose `department` matches `'Sales'` or `'Finance'`.

## Retrieve all employees not in IT

*Your team needs to make one more update to employee machines. The employees who are in the Information Technology department already had this update, but employees in all other departments need it. Use filters in SQL to create a query which identifies all employees not in the IT department. (The department of the employee is found in the `department` column, which contains values that include `Information Technology`.)*

```SQL
SELECT *
FROM employees
WHERE NOT department = 'Information Technology';
```

This query will return all the records from `employees` whose `department` is anything but `'Information Technology'`.

## Summary

I used SQL queries to get the required information for each situation. I used two tables, `log_in_attempts` and `employees`. I also used the `AND`, `OR`, and `NOT` operators to filter information. I also used `LIKE` with the percentage sign (`%`) wildcard to filter for patterns.
