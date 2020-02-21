# GAM IMAP Settings

##### Determine IMAP Status on Users in an OU
    gam ou <OrganizationalUnit> show imap > IMAP.csv

##### Enable IMAP on a Single Account
    gam user aamco_stop_request@Domain imap on

##### Enable IMAP for an Entire OU of Accounts
    gam ou <OrganizationalUnit> imap on
