# GAM - Commands and Scripts for GAM Google API

Quick Reference - https://gamcheatsheet.com/

GAM Repo - https://github.com/jay0lee/GAM

Search Operators in G Suite - https://support.google.com/mail/answer/7190?hl=en

# Syntax

gam user <username>  forward on|off  <EmailAddress> delete

    Who - forward on or off - where to - the action to take on the original mailbox item


# Forward and Filter (migration)
gam user USER@reachlocal.com add forwardingaddress USER_FWD@reachlocal.gannett.com
gam user USER@reachlocal.com forward on USER_FWD@reachlocal.gannett.com delete
gam user USER@reachlocal.com filter from USER@reachlocal.com trash

# Show Results on Single User
gam user USER@reachlocal.com show forward > ShowFWD.csv
gam user USER@reachlocal.com show filter > ShowFilter.csv

# INFO
Gam info group naserviceleaders@reachlocal.com
Gam info user khaughey@reachlocal.com

# NOT SURE WHAT AN OBJECT IS?
Gam whatis publisher-ops@reachlocal.com

# Identifiy Filter
gam user USER@domain show filters

# Remove Filter:
gam user eddie.valdez@reachlocal.com delete filters ANe1Bmj7YST9EbOjouCIBluj3FEhcBrTjmAa8w

# Turn Off and Delete Forward on Single User (for correcting a FWD)
gam user USER@reachlocal.com forward off USER_FWD@reachlocal.gannett.com
gam user USER@reachlocal.com delete forwardingaddress USER_FWD@reachlocal.gannett.com

# Run Forward and Filter on CSV of Users (RUN THESE ONE AT A TIME)*
gam csv USERCSV.csv gam user ~Source add forwardingaddress ~Destination > Output_ForwardAdd.csv
gam csv USERCSV.csv gam user ~Source forward on ~Destination delete  > Output_ForwardOn.csv
gam csv USERCSV.csv gam user ~Source filter from ~Source trash > AU_B2_Cutover_Output_Filter.csv

# Show Results on CSV of Users
gam csv USERCSV.csv gam user ~Source show forward > Output_ShowForward.csv
gam csv USERCSV.csv gam user ~Source show filter > Output_ShowFilter.csv

# Remove Filter for User
gam user USER@reachlocal.com show filters

# Find filter ID you wish to delete
gam user USER@domain.com delete filters <FilterID>
gam user khaughey@reachlocal.com delete filters ANe1BmglaeY1T4uXQzqJicElCawI8omcLdkOr

# Add Google Enterprise License to User
gam user USER@reachlocal.com add license 1010020020

# Format for CSV (case sensitive headers)
Source,Destination
khaughey@reachlocal.com,khaughey@reachlocal.gannett.com
aabad@reachlocal.com,aabad@reachlocal.gannett.com

# Email Query and Deletion by Label

## Query ONLY Messages with Label
gam user USER@reachlocal.com delete messages query label:Trash

# Query and DELETE Messages with Label (WARNING!)
gam user USER@reachlocal.com delete messages query label:Trash doit maxtodelete 999999999

# Query and DELETE Messages with Label older than 1 Year with Label (WARNING!)
gam user USER@reachlocal.com delete messages query older_than:y query label:Trash doit maxtodelete 999999999

# Query and DELETE Messages from Before 1/1/2018 with Label (WARNING!)
gam user USER@reachlocal.com delete messages query before:2018/01/01 query label:Trash doit maxtodelete 999999999

# Batch Statements to Run  

## Save statements one per line to txt format, then launch with the following:
gam batch TXTFILE.txt > Output.csv


