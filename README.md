## Training Data

This repository stores training data for the 
[statistical inference component](https://github.com/REMEXLabs/GPII-Statistical-Matchmaker-Analysis) 
of the GPII Statistical matchmaker.

## Format

The preference set format is an .ini file, for more information about comments and syntax see 
[Wikipedia](http://en.wikipedia.org/wiki/INI_file)

In INI files, key-value pairs are written as 

    key=value

To make it easier to copy over data from JSON files, the Statistical Analaysis also allows storing key-value pairs as

    "key": "value"
	
Each file represents one particular set of application settings for a single context configuration. Note that one hierarchical GPII preference set can end up forming multiple .ini files for inference.

### [context] Section

The context section stores key-value pairs defining the context of this whole file. There should only be one [context] section per file.

### [preferences] Sections

The preference sections store key-value pairs defining settings for a certain application.

A preference Section needs to have one key-value pair for "app", defining which application the preference section is for.

Multiple preference sections can be used to define settings for multiple applications.

## Available Data Sets

### dataSecondPhase

Training data based on preference sets that were created during the second round of user testing in the Cloud4all project. 

### generatedDataThirdPhase

Training data that were generated semi-automatically to support demonstration scenarios in January 2015.

### manualDataSecondPhase

Manually created training data to support the test scenarios in the second round of user testing in the Cloud4all project.
These training data should be considered as "legacy data". 
They can still be used for comparison with statistical matchmaker from the third pilot phase, 
provided that the differences with the newer training data are taken into account. 

### manualDataThirdPhase 

Manually created training data to support the test scenarios in the third round of user testing in the Cloud4all project.
These data should not be combined with training data from previous evaluation phases.

The manually created training data for the third evaluation phase consist of the following categories:
* An updated version of the manual data for the second phase. The main characteristics of this update are:
  ** The addition of settings expressed as "common terms" (or "common format terms").
  ** The addition of the setting `_disabled=true` where more than one solution in the same category is available and only one should be launched (e.g. to make sure that only NVDA gets launched when there one or more other screen readers are available on the same system).
  ** `=` (instead of colons) are now used consistently between key-value pairs.
* New data for a few new solutions.
* Data that focus on specific settings instead of entire solutions or groups of settings. Example: speech rate in various screen readers, magnification in various magnifiers, and user interface language in various solutions.

## Funding Acknowledgement

The research leading to these results has received funding from the European
Union's Seventh Framework Programme (FP7/2007-2013) under grant agreement No.289016
([Cloud4all](http://www.cloud4all.info/)).

