# Consolidating-Employee-Data
Use DataFrames to read and merge employee data from different sources.

# Description:
Data comes in different shapes, sizes, and formats. The ability to merge and clean different sources for analysis is a fundamental skill for any data practitioner.

In this project you'll do just that, working with human resources data in CSV, Excel, and JSON format.

# Project Instructions
Read in, merge, and clean the four datasets to make a single combined pandas DataFrame.

Create a single pandas DataFrame called employees_final containing:
Index: employee_id.
Columns: Ensure the DataFrame contains only the following columns, in the exact order listed: employee_first_name, employee_last_name, employee_country, employee_city, employee_street, employee_street_number, emergency_contact, emergency_contact_number, relationship, monthly_salary, team, title, office, office_country, office_city, office_street, office_street_number.
Assign employees to offices based on their country. For any columns that begin with office, replace missing data with "Remote".

You just got hired as the first and only data practitioner at a small business experiencing exponential growth. The company needs more structured processes, guidelines, and standards. Your first mission is to structure the human resources data. The data is currently scattered across teams and files and comes in various formats: Excel files, CSVs, JSON files...

You'll work with the following data in the `datasets` folder:
- __Office addresses__
    - Saved in `office_addresses.csv`. 
    - If the value for office is `NaN`, then the employee is remote.
- __Employee addresses__
    - Saved on the first tab of `employee_information.xlsx`.
- __Employee emergency contacts__ 
    - Saved on the second tab of `employee_information.xlsx`; this tab is called `emergency_contacts`. 
    - However, this sheet was edited at some point, and ***the headers were removed***! The HR manager let you know that they should be: `employee_id`, `last_name`, `first_name`, `emergency_contact`, `emergency_contact_number`, and `relationship`.
- __Employee roles, teams, and salaries__ 
    - This information has been exported from the company's human resources management system into a JSON file titled `employee_roles.json`. Here are the first few lines of that file:
```
{"A2R5H9":
  {
    "title": "CEO",
    "monthly_salary": "$4500",
    "team": "Leadership"
  },
 ...
}
```
