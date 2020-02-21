# GAM Labels

##### Show Labels for an Account
    gam user USER@Domain show labels

##### Rename a Label
    gam user USER@Domain update labelsettings OldLabelName name NewLabelName

##### Rename Labels from a List
    gam csv Duplicate_Contacts_Label.txt gam user ~Email update labelsettings OldLabelName name NewLabelName > LabelRename.csv
