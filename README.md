# Flight Data Reconciliation Process
##### _A process automation for reconciling flights data using Blueprism v.6.10_

This process automatio has been developed using Bluerism RPA tool with following Business Objects
- Utility - Environment
- Utility - General
- Data - OLEDB
- Utility - Strings
- Utility - Collection Manipulation
- MS Excel VBO

#### Processing Steps :

- The flights data CSV file is generated having multiple segment columns which need to be split into different rows of it's own. 

- We are using OLEDB VBO to read the CSV file and then we we use a series of actions using Regular Expressions and Collection Manipulation activity to transform the data into a readable data table. 

- Finally we write the datatable by creating a new excel file.
- 
#### Custom Actions Created :

Add Fields To Collection

This action has been created to dynamically add field names to an existing collection at run time based on a list of input field names.

This action has been created to dynamically add field names to an existing collection at run time based on a list of input field names.
| Parameter         | Direction | Data Type  | Description                                                                                                                                                                                   |
|-------------------|-----------|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Input Collection  | In        | Collection | The input collection where the fields will be added dynamically during runtime.                                                                                                               |
| Fields            | In        | Collection | The fields collection which consists of the list of fields to be added. NOTE : The fields collection must have a single column called Field Name consisting of field names in different rows. |
| - Field Name      | In        | Text       | The field names to be added.                                                                                                                                                                  |
| - Field Type      | In        | Text       | The field type to be added. Possible types are : String, Integer, Date, Decimal, Boolean, DateTime.                                                                                           |
| Output Collection | Out       | Collection | The output collection which consists of all the fields described in the input of the action.                                                                                                  |
