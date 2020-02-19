#Move user to new OU
gam update org <OrganizationalUnit> add users USER@Domain

#Add list of users to an OU
gam update org <OrganizationalUnit> add file FinalAccountList.txt

#Print list of users in an OU
gam print users query "orgUnitPath=/<OrganizationalUnit>" > FileName.csv
