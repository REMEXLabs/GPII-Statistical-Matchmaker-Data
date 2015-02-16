## Training Data

This repository stores training data for the 
[statistical inference component](https://github.com/REMEXLabs/GPII-Statistical-Matchmaker-Analysis) 
of the GPII Statistical matchmaker.
	
## Format

The preference set format is an .ini file, for more information about comments and syntax see http://en.wikipedia.org/wiki/INI_file

In INI files, key-value pairs are written as 

    key=value

For easier copying out of JSON formats, the Statistical Analaysis also allows storing key-value pairs as

    "key": "value"
	
Each file represents one particular set of application settings for a single context configuration. Note that one hierarchical GPII preference set can end up forming multiple .ini files for inference.

### [context] Section

The context section stores key-value pairs defining the context of this whole file. There should only be one [context] section per file.

### [preferences] Sections

The preference sections store key-value pairs defining settings for a certain application.

A preference Section needs to have one key-value pair for "app", defining which application the preference section is for.

Multiple preference sections can be used to define settings for multiple applications.



## Funding Acknowledgement

The research leading to these results has received funding from the European
Union's Seventh Framework Programme (FP7/2007-2013) under grant agreement No.289016
([Cloud4all](http://www.cloud4all.info/)).
