# GAM Calendars

>Format

    gam calendar <calendar email> add freebusy|read|editor|owner <user email>

#### Show Calendar ACL

      gam calendar Domain_35333539353737323734@resource.calendar.google.com showacl

#### Add user as owner to calendar

    gam csv List.csv gam calendar ~Email add owner ~Owner

    gam calendar ~Email showacl > Output.csv

#### Get All Calendars for a List of Groups

    gam csv List.csv gam group ~Email show calendars > FileName.csv
    
