# GAM Filters

##### Filter from self to trash
    gam user USER@Domain filter from USER@NewDomain trash

##### All Email Bypass SPAM
    gam user USER@Domain filter from '*' neverspam

##### Emails from List to Bypass SPAM
    gam csv FILE.csv gam user ~User filter from '*' neverspam

    gam csv FILE.csv gam user ~User show filter > NeverSpam_AU.csv

##### Remove Filter(s)
    gam user <username>|group <groupname>|ou <ouname>|all users delete filters <FilterIDList>
