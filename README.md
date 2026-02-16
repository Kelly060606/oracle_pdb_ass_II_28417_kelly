# Oracle Pluggable Database Assignment

## Student Information
- **Name:** Kelly
- **Student ID:** 28417

## Oracle Environment
- Oracle Database 21c Express Edition
- Windows 10

## Task 1: Create PDB
I created a pluggable database named `ke_pdb_28417` with admin user `kelly_plsqlacua_28417`. 
When I first ran the CREATE command, I got an ORA-65005 error because my file path was incorrect. 
The error message showed the correct path (C:\APP\HP\PRODUCT\21c\DEINSTALL2025-05-06_12-01-18PM\ORADATA\XE\PDBSEED\), 
so I updated my command and the PDB created successfully. 
I then opened it with ALTER PLUGGABLE DATABASE...OPEN and saved its state. 
Running SELECT FROM v$pdbs confirmed my PDB shows "READ WRITE" mode.

## Task 2: Create and Delete Temporary PDB
I created a temporary PDB called `ke_to_delete_pdb_28417` using the same file paths.
The creation worked immediately. When I tried to close it, I got an error saying it was 
"already closed," so I skipped directly to the DROP command. 
After dropping it with INCLUDING DATAFILES, I ran the verification query and saw 
"no rows selected" — confirming it was completely gone.

## Task 3: Oracle Enterprise Manager
I accessed OEM Express at https://localhost:5500/em and logged in as SYS with my password.
The dashboard loaded showing various graphs and performance metrics. 
At the top right corner, I could see my username "SYS" displayed. 
Under the Data Storage section, I saw `ke_pdb_28417` listed with its size, 
confirming my PDB exists and OEM is working correctly.

## Challenges Faced
The main challenge was the file path error during PDB creation. 
The error message showed the correct path with the timestamp folder (DEINSTALL2025-05-06...), 
which I used to fix my command. Another small issue was trying to close an already-closed 
PDB in Task 2, but I learned I could skip that step.

## Integrity Statement
"I confirm that this work is my own execution and all screenshots represent 
my actual work on Oracle 21c. No part of this assignment was copied from others."
