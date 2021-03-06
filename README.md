# v4.2
https://cdn.jsdelivr.net/gh/access2vivek/iMacrosDatabase@c7cff8f1/v4.2.js

Changed many of the methods so that they are optimum. Removed unnecessary methods to speed up the code.

# v4.1
https://cdn.jsdelivr.net/gh/access2vivek/iMacrosDatabase@61cb1d7a/v4.1.js

Modified **upload** and **read** to take care of *currentRow* variable.

# v4.0
https://cdn.jsdelivr.net/gh/access2vivek/iMacrosDatabase@bba95004/v4.0.js

## addSP(object)
Replaces space with "<SP>" in "folder" and "fileName".


## removeSP(object)
Replaces "<SP>" with space in "folder" and "fileName".

  
## clearDisplay()
Removes any text from iimDisplay.


## getPath(object)
**Returns** *folder* followed by backslash(\) followed by *fileName*


## exists(object)
Calls **addSP(object)** then checks if file exists. 

**Returns** true/false.


## rowExists(object,rowNumber)
Calls **addSP(object)** then checks if row specified by rowNumber exists.

**Returns** true/false.

## uploadFile(object,message)
Opens the upload file dialog for uploading the file with the given *message*.

Sets the "folder" and "fileName" variables.

**Returns** true/false.

## uploadFolder(object,message)
Opens the select folder dialog with the given *message*.

- [x] Make the method return true/false.

## delete(object)
Calls **addSP(object)** and checks if file exists.

Deletes the file specified by the object's folder and fileName.

**Returns** true if the file was deleted.

**Returns** false if the file did not exist or there was trouble deleting it.

## read(object,rowNumber)
Calls **addSP(object)** then checks if the row specified by *rowNumber* exists in the file.

Sets the *currentRow* variable to *rowNumber* if the file and the row exist.

Reads the entire row and sets the *values* array.

Clears the iimDisplay.

**Returns** true if the values were read.

**Returns** false if the row specified by *rowNumber* does not exist.

## readFull(object)
Calls **addSP(object)**

Assumes that the file specified by *object* exists.

**Returns** the entire contents of a specified file (CSV/TXT).

## write(object,data)
Calls **addSP(object)**

Makes an row entry in the file specified by *object*.

The *data* variable is an array that contains all the values to insert.

## getHeaders(object,headers)
Reads the first row of the file specified in the *object* variable.

Sets the values of *headers* variable array to the first row of the file.

## setFolder(object,folder)
Sets the "folder" variable of the *object* variable to the *folder* parameter.

## setFileName(object,fileName)
Sets the "fileName" variable of the *object* variable to the *fileName* parameter.

## setFile(object,folder,fileName)
Sets the "folder" and "fileName" variable of the *object* variable to *folder* and *fileName* parameters respectively.

## To-Do
