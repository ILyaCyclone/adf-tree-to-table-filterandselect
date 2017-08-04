# adf-tree-to-table-filterandselect

A small Oracle ADF example of a tree filtering a table and selecting its row.
Model is based on on standard Oracle HR.
The example is exposing this hierarchy:
> Locations
>> Departments
>>> Employees

To run the example you must provide a suitable database connection to HR schema.
To do this in Applications window open Application Resources - Connections - Database - hr@test and set needed connection values.

You may also want to remove custom timezone configuration needed in my environment. To do so right click on ViewController project - Project Properties and in Run/Debug section select Default run configuration. Click OK and restart application server.

When the example is running in your browser:

1. In the tree select Texas - IT - Valli Pataballa.

You should see all IT department employees in the table and Valli Pataballa selected.
![Texas - IT](http://i.imgur.com/xBwZ09c.png)

2. Select Oxford - Sales - Peter Hall.

You should see all Sales department employees in the table and Peter Hall selected.
![Oxford - Sales](http://i.imgur.com/DFtVBZJ.png)

If that is so, your filtration and selection is working properly.

The key part of the filtration and selection is Target Data Source attribute.
You can find it in your tree binding.
We use it on Departments tree level to filter the table to the right; and on Employees tree level to select table row.

1. Departments Target Data Source

This will select DepartmentsView1Iterator row a hence filtering employees table.
![Departments Target Data Source](http://i.imgur.com/PEFKnS4.png)

2. Employees Target Data Source

This will select EmployeesView1Iterator row making employees table selection.
![Employees Target Data Source](http://i.imgur.com/amUPCYl.png)

Oracle ADF/JDeveloper 12.1.3
