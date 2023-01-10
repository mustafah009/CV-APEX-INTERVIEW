# CV-APEX-INTERVIEW

- Fork this repository
- Create account in https://apex.oracle.com/en/
- Request Workspace
- Data Model
    - Quick SQL script

    ```
    jobs /insert 4
    name /upper /unique /check developer, analyst, manager, assistant
    departments /insert 5
    name vc100 /nn /upper /unique /check hr, development, legal, sales, operations
    cost center num
    employees /insert 100
        first_name
        last_name
        email /lower
        hire_date
        city
        country
        job id /references jobs
    

- Create an apex application manage employees:
- Create page manage employee:
    - Create region with dashboard on the name that includes:
         - 1 badge with total number of employees
         - 1 bar chart with number of employees per department
     - Create region with employee report on the name that includes:
         - 2 interactive grids defined as master / detail
             - Grids to be implemented based on APEX collections
             - The master interactive grid will have the following functionality:
                 - Add Add/Remove buttons to the interactive grid toolbar
                 - Add button will add a new line to the Interactive Grid and will allow for department selection from a lov of departments
                 - Implement remove departments with an AJAX callback
             - The detail interactive grid will have the following functionallity:
                 - Add Add/Remove buttons to the interactive grid toolbar
                 - Add button will open a popup dialog to search for an employee and will have a OK/Close button
                     - OK persists employee to the collection
                     - Close, closes the dialog
                 - Remove button will remove users with an AJAX callback
 - Save button at application page level
     - Will ask for confirmation before saving only if there's any pending changes in the collections