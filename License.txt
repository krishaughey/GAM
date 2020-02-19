#Print Licenses (list of users) by Product (Google-Apps)
gam print licenses products Google-Apps > FileName.csv

#Change to a Vault Former Employee License from List of User Emails
gam csv TermedUsers.csv gam user ~Email add license Google-Vault-Former-Employee > FileName.csv

#Change to a Google Enterpise License
gam user USER@Domain add license 1010020020

#Remove a license from an OU of Users
gam ou <OrganizationalUnit>/<Sub-OrganizationalUnit> delete license Google-Vault-Former-Employee

#Add a license to an OU of Users
gam ou <OrganizationalUnit>/<Sub-OrganizationalUnit> add license 1010020020
