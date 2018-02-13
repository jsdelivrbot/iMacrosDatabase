# iMacrosDatabase
All the methods for Database Handling

## v4.0

### addSP(object)
Replaces space with "<SP>" in "folder" and "fileName".


### removeSP(object)
Replaces "<SP>" with space in "folder" and "fileName".

  
### clearDisplay()
Removes any text from iimDisplay.


### getPath(object)
**Returns** *folder* followed by backslash(\) followed by *fileName*


### exists(object)
Calls **addSP(object)** then checks if file exists. 
**Returns** true/false.


### rowExists(object,rowNumber)
Calls **addSP(object)** then checks if row specified by rowNumber exists. 
**Returns** true/false.

### uploadFile(object,message)
Opens the upload file dialog for uploading the file with the given *message*.
Sets the "folder" and "fileName" variables.
**Returns** true/false.

### uploadFolder(object,message)
Opens the select folder dialog with the given *message*.
[] Make the method return true/false.

### delete(object)
Calls **addSP(object)** and checks if file exists.
Deletes the file specified by the object's folder and fileName.
**Returns** true if the file was deleted.
**Returns** false if the file did not exist or there was trouble deleting it.

### read(object,rowNumber)
Calls **addSP(object)** then checks if the row specified by *rowNumber* exists in the file.
Sets the *currentRow* variable to *rowNumber* if the file and the row exist.
Reads the entire row and sets the *values* array.
Clears the iimDisplay.
**Returns** true if the values were read.
**Returns** false if the row specified by *rowNumber* does not exist.

### readFull(object)
Calls **addSP(object)**
Assumes that the file specified by *object* exists.
**Returns** the entire contents of a specified file (CSV/TXT).

### write(object,data)
Calls **addSP(object)**
Makes an row entry in the file specified by *object*.
The *data* variable is an array that contains all the values to insert.
