# GAM Drive

>Format

    gam <who> print teamdrives todrive

#### Printing Team Drives
      gam ou <OrganizationalUnit> print teamdrives todrive

      gam ou <OrganizationalUnit> print teamdrives allfields todrive

      gam ou <OrganizationalUnit> print teamdrives todrive

#### Show File List
      gam ou <OrganizationalUnit> show filelist allfields todrive

      gam ou <OrganizationalUnit> show filelist query "mimeType = 'application/pdf'"

      gam ou <OrganizationalUnit> show filelist query "fullText contains 'Oracle'"

##### Pull from list of users - get all drive info to csv
    gam csv GSA-Users1.csv gam show filelist allfields > Drive_Report_1.csv

##### Drive Report from List
    gam csv DrvGrp_A.csv gam user ~primaryEmail show filelist name shared permissions > DriveReport_Group_A.csv

##### Report on User's Storage Usage
      gam report users parameters accounts:drive_used_quota_in_mb,accounts:gmail_used_quota_in_mb todrive

##### Change Ownership of Specific Drive Item (Using ID)
    gam user OldOwner@domain.com update drivefileacl 0ByS7P5FlrbOT NewOwner@domain.com role owner

##### Add User to File as Writer
    gam user NewWriter@Domain add drivefileacl 1-BIyyl9-VC5VZy2_cpCR32Yr3JDVGkhHvbtf48zLSJ4 user USER@Domain role writer

##### Add User to File as Writer via CSV
    gam csv DriveFile_Writer.csv gam user ~Owner add drivefileacl ~File user ~Writer1 user ~Writer2 role writer

##### User with domain-shared files
    gam user USER@Domain show filelist query "visibility = 'domainWithLink'" > FileName.csv

##### Users in specific OU with domain-shared files
    gam ou <OrganizationalUnit> show filelist query "visibility = 'domainWithLink'" > FileName.csv

##### User to User Transfer (Drive)
    gam create datatransfer USER@Domain drive USER2@Domain

      gam csv TransfterTest.csv gam create datatransfer ~Owner drive ~Transfer

##### Report from FileID on Changes (looking for possible Owner)
    gam report drive user all filters "doc_id==0AJG9NfqTcB5YUk9PVA"
