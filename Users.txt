#Print Users Matching Query Prefix
gam print users query “email:vfe*” > vfe.txt

#Print Users Matching Domain
gam print users emails query 'email:Domain' > FileName.csv

#Print users from a specific OU
gam print users query "orgUnitPath=/<OrganizationalUnit>" > FileName.csv

gam report users parameters accounts:drive_used_quota_in_mb,accounts:gmail_used_quota_in_mb todrive

gam print users emails todrive
