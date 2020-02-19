# GAM - Commands and Scripts for GAM Google API

Quick Reference - https://gamcheatsheet.com/

GAM Repo - https://github.com/jay0lee/GAM

Search Operators in G Suite - https://support.google.com/mail/answer/7190?hl=en

# Account Info
    Gam info group GROUP@Domain

    Gam info user USER@Domain

    Gam whatis ACCOUNT@Domain

# Add Google Enterprise License to User
    gam user USER@Domain add license 1010020020

# Forward and Filter
    gam user USER@Domain add forwardingaddress USER_FWD@NewDomain
    gam user USER@Domain forward on USER_FWD@NewDomain delete
    gam user USER@Domain filter from USER@Domain trash

    gam user USER@Domain show forward > ShowFWD.csv
    gam user USER@Domain show filter > ShowFilter.csv

    gam user USER@Domain forward off USER_FWD@NewDomain

    gam user USER@Domain.com delete filters <FilterID>

# Query/Delete Messages by Label ("doit" executes)
    gam user USER@Domain delete messages query label:Trash

    gam user USER@Domain delete messages query label:Trash doit maxtodelete 999999999

# Delete Messages with Label older than 1 Year with Label ("doit" executes)
    gam user USER@Domain delete messages query older_than:y query label:Trash doit maxtodelete 999999999

# Delete Messages from Before DATE with Label ("doit" executes)
    gam user USER@Domain delete messages query before:YYYY/MM/DD query label:Trash doit maxtodelete 999999999          

#  CSV format (case sensitive headers)
    Source,Destination
    USER@Domain,USER@NewDomain
    USER@Domain,USER@NewDomain

# Run Forward and Filter on List
    gam csv USERCSV.csv gam user ~Source add forwardingaddress ~Destination > Output_ForwardAdd.csv
    gam csv USERCSV.csv gam user ~Source forward on ~Destination delete  > Output_ForwardOn.csv
    gam csv USERCSV.csv gam user ~Source filter from ~Source trash > AU_B2_Cutover_Output_Filter.csv

    gam csv USERCSV.csv gam user ~Source show forward > Output_ShowForward.csv
    gam csv USERCSV.csv gam user ~Source show filter > Output_ShowFilter.csv
