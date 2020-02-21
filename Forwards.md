# GAM Forwarding

    gam <who> forward on|off [email address] [keep|archive|delete]


    gam user USER@Domain show forwardingaddresses

    gam user USER@Domain add forwardingaddress USER@NewDomain

    gam user USER@Domain forward on USER@NewDomain keep

#### Delete Forward
    gam user <username>|group <groupname>|ou <ouname>|all users delete forwardingaddress <EmailAddress>


    gam user USER@Domain delete forwardingaddress USER@NewDomain

#### Forward and Filter  
    gam user USER@Domain add forwardingaddress USER_FWD@NewDomain
    gam user USER@Domain forward on USER_FWD@NewDomain delete
    gam user USER@Domain filter from USER@Domain trash

    gam user USER@Domain show forward > ShowFWD.csv
    gam user USER@Domain show filter > ShowFilter.csv

    gam user USER@Domain forward off USER_FWD@NewDomain

    gam user USER@Domain.com delete filters <FilterID>
