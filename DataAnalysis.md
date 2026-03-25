# Basic insights from the data
* Understand your data before you begin any analysis
* Should check:
    * Data types (```df.dtypes``` or ```df.info()```)
        * potential info and type mismatch
        * compatibility with python methods
    * Data distribution (```df.describe(include="all")```)
* Locate potential issues with the data

# Accessing Databases - using DB-API
```
from dmodule import connect

# Create connection object
connection = connect('databasename','username','pswd')

# Create a cursor object
cursor = connection.cursor()

# Run queries
cursor.execute('select * from mytable')
results = cursor.fetchall()

# Free resources
cursor.close()
connection.close()
```

# How to deal with missing data
* Check with the data collection source
* Drop the missing value
    * drop the variable
    * drop the data entry
* Replace the missing values
    * replace it with an average(of similar datapoints)
    * replace it by frequency (if type is object)
    * replace it based on other functions (additional info that you know)
* Leave it as missing data