# synthetic-mwl-sample-pack

Synthetic DICOM MWL Sample Dataset
==================================

This repository contains a small ready-to-use synthetic DICOM Modality Worklist (MWL) dataset
for evaluation and testing.

It is intended for developers, integrators and QA engineers working with DICOM-based systems.


WHAT IS INCLUDED
----------------
This sample pack contains:
- CSV export of MWL items (flat structure)
- JSON export of MWL items (structured format)
- Metadata file
- Sample README

Each row/item represents one Scheduled Procedure Step (SPS).


PURPOSE
-------
This dataset can be used to:
- test MWL import pipelines
- validate mappings
- simulate MWL worklist queries
- develop modality integrations
- test PACS / RIS workflows
- validate DICOM header prepopulation


IMPORTANT CONCEPT
-----------------
1 procedure = 1 MWL worklist item

This means:
- a patient may appear multiple times
- each entry represents a scheduled procedure
- this is expected MWL behavior


WHAT IS NOT INCLUDED
--------------------
This repository does NOT provide:
- a DICOM MWL server
- C-FIND implementation
- PACS or RIS
- production clinical data
- real patient data

The data must be imported into or mapped to your own test environment.


TEST DATE
---------
The dataset is generated for:
  2026-05-11

Many devices query only the current date.

If your worklist appears empty:
- check system date / NTP
- ensure query date matches the dataset date
- or regenerate dataset for the required test date


ENCODING
--------
ASCII-normalized for compatibility:
  Müller -> MUELLER
  Köln   -> Koeln
  Straße -> Strasse


PACKAGE STRUCTURE
-----------------
Synthetic_MWL_SamplePack_2026-05-11/
  csv/
    mwl_items_2026-05-11.csv
  json/
    mwl_items_2026-05-11.json
  metadata.json
  README.txt


EXAMPLE FIELDS
--------------
Typical fields include:
- PatientID
- PatientName
- PatientBirthDate
- PatientSex
- AccessionNumber
- ScheduledProcedureStepID
- ScheduledProcedureStepStartDate
- ScheduledProcedureStepStartTime
- Modality
- Department


SYNTHETIC DATA NOTICE
---------------------
This dataset contains synthetic test data only.
- no real patient data
- not for clinical use
- intended for testing and development


NEXT STEPS
----------
For larger datasets you can generate or request:
- single-day datasets (50+ items)
- monthly datasets
- specific modality profiles
- custom distributions
- Unicode variants


TARGET USERS
------------
- DICOM developers
- healthcare integrators
- QA engineers
- PACS / RIS developers


LICENSE
-------
This dataset is released under the MIT License.
Use it for testing and development.
