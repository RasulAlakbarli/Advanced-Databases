# Advanced Databases

## Course 1 

In databases, particularly in the context of **relational algebra**, various symbols and terms are used to describe operations on relational databases. Here’s a list of the most common terminology:

1. **Selection (σ)**:  
   - **Notation**: \( \sigma_{condition}(R) \)
   - **Operation**: Selects rows from a relation (table) that satisfy a given condition.
   - **Example**: \( \sigma_{age > 30}(Employees) \) selects all employees older than 30.

2. **Projection (π)**:  
   - **Notation**: \( \pi_{attributes}(R) \)
   - **Operation**: Selects specific columns from a relation.
   - **Example**: \( \pi_{name, salary}(Employees) \) projects the `name` and `salary` columns from the `Employees` relation.

3. **Renaming (ρ)**:  
   - **Notation**: \( \rho_{new\_name}(R) \)
   - **Operation**: Renames a relation or attributes in a relation.
   - **Example**: \( \rho_{Emp}(Employees) \) renames the `Employees` relation to `Emp`.

4. **Union (∪)**:  
   - **Notation**: \( R_1 \cup R_2 \)
   - **Operation**: Combines the tuples from two relations. Duplicate rows are removed.
   - **Example**: \( Employees \cup Managers \) returns all employees and managers, without duplicates.

5. **Intersection (∩)**:  
   - **Notation**: \( R_1 \cap R_2 \)
   - **Operation**: Returns tuples that are common to both relations.
   - **Example**: \( Employees \cap Managers \) returns tuples that are in both `Employees` and `Managers`.

6. **Difference (−)**:  
   - **Notation**: \( R_1 - R_2 \)
   - **Operation**: Returns tuples from the first relation that are not in the second relation.
   - **Example**: \( Employees - Managers \) returns employees who are not managers.

7. **Cartesian Product (×)**:  
   - **Notation**: \( R_1 \times R_2 \)
   - **Operation**: Returns the Cartesian product (all possible combinations of rows) of two relations.
   - **Example**: \( Employees \times Departments \) gives all combinations of employee-department pairs.

8. **Join (⨝)**:  
   - **Notation**: \( R_1 \bowtie_{condition} R_2 \)
   - **Operation**: Combines tuples from two relations based on a related condition.
   - **Example**: \( Employees \bowtie_{Employees.dept = Departments.dept} Departments \) joins `Employees` and `Departments` based on the `dept` attribute.

9. **Natural Join (⋈)**:  
   - **Notation**: \( R_1 \bowtie R_2 \)
   - **Operation**: Joins two relations by implicitly matching all attributes with the same name.
   - **Example**: If `Employees` and `Departments` both have a `dept` attribute, \( Employees \bowtie Departments \) joins them on the `dept` attribute.

10. **Theta Join (⨝ θ)**:  
    - **Notation**: \( R_1 \bowtie_{\theta} R_2 \)
    - **Operation**: A more general join that allows any comparison operator (e.g., <, >, =).
    - **Example**: \( Employees \bowtie_{Employees.salary > Departments.budget} Departments \) joins `Employees` and `Departments` where the employee's salary is greater than the department's budget.

11. **Division (÷)**:  
    - **Notation**: \( R_1 \div R_2 \)
    - **Operation**: Returns tuples in \( R_1 \) that are related to all tuples in \( R_2 \).
    - **Example**: If `Projects` is divided by `Managers`, it returns managers who are involved in all projects.

12. **Aggregation (G)**:  
    - **Notation**: \( G_{attributes; function}(R) \)
    - **Operation**: Groups the relation by some attributes and applies aggregate functions like SUM, AVG, COUNT, etc.
    - **Example**: \( G_{dept; SUM(salary)}(Employees) \) returns the total salary for each department.

These symbols and operations form the foundation of query languages like SQL and are essential in understanding relational database theory.
