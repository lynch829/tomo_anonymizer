TomoTherapy Batch Archive Anonymizer
===========

by Mark Geurts <mark.w.geurts@gmail.com>
<br>Copyright &copy; 2014, University of Wisconsin Board of Regents

AnonymizeDatasets scans a folder for TomoTherapy&reg; patient archives. For each archive found, the patient's name and MRN are removed, the archive signature file is deleted, and the folder is renamed.  Patient names/folders will be renamed incrementally (Anon_0001, Anon_0002, etc).  Note, the original and new archive names are recorded using the `Event()` function to the file log.txt.  Therefore, to remove any connection of the original and anonymized archives, this file should be deleted following execution.

WARNING: THIS WILL MODIFY ALL PATIENT ARCHIVES, RENDERING THEM UNABLE TO RESTORE BACK TO A TOMOTHERAPY DATABASE.

TomoTherapy is a registered trademark of Accuray Incorporated.

## Contents

* [MATLAB Function Use](README.md#matlab-function-use)
* [Example](README.md#example)
* [License](README.md#license)

## MATLAB Function Use

The following variables are required for proper execution: 

* varargin{1}: folder to search for archives (relative to the MATLAB path)
*  varargin{2} (optional): integer to use for renaming patients.  The count will start with this integer, and increment by one for each subsequent archive found.  If not included, the count will start at one.

No variables are returned.

## Example

```matlab
folder = './Archives'; % Folder containing the archives
startNum = 11; % Start numbering at 11
AnonymizeDatasets(folder, startNum);
```

## License

This program is free software: you can redistribute it and/or modify it 
under the terms of the GNU General Public License as published by the  
Free Software Foundation, either version 3 of the License, or (at your 
option) any later version.

This program is distributed in the hope that it will be useful, but 
WITHOUT ANY WARRANTY; without even the implied warranty of 
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE. See the GNU General 
Public License for more details.

You should have received a copy of the GNU General Public License along 
with this program. If not, see http://www.gnu.org/licenses/.
