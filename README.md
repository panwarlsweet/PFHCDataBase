# PFHCDataBase
This repository contains all the records of files related to updates in PF Hadron Calibration. TWiki: https://twiki.cern.ch/twiki/bin/view/CMS/PFCalibrationDBConditions The details of each folder is as follows:

# PDF: 
Slides/Results or related documentation with updates in PF Hadron Calibration

# textfiles: 
To store all the metadata text files

# SQLiteFiles: 
To store .db file correcspinding to the metadata text files. 

# xmlfiles
To create xml files correspoding to each Tag follow these steps in PFHCDataBase directory within CMSSW environment: 

"""
conddb --db /path/fileName.db  list TagName
"""
it will show unique Payload hash of the payload (simiar to this c85fdfbbca045de26ae6e641763c61c42ff6ab39). To generate xml file write:

"""
conddb  dump PayloadHash >  PFCalibration.xml

(for ex.) conddb  dump c85fdfbbca045de26ae6e641763c61c42ff6ab39 >  PFCalibration.xml
"""
now xml file is ready. One can commit this in GitHub
