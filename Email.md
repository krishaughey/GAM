# GAM Email

##### Query Messages with Label to Delete
    gam user USER@Domain delete messages query label:Trash

##### Query and DELETE Messages with Label
    gam user USER@Domain delete messages query label:Trash doit maxtodelete 999999999

##### Query and DELETE Messages with Label older than 1 Year with Label
    gam user USER@Domain delete messages query older_than:y query label:Trash doit maxtodelete 999999999

##### Query and DELETE Messages from Before 1/1/2018 with Label
    gam user USER@Domain delete messages query before:2018/01/01 query label:Trash doit maxtodelete 999999999
