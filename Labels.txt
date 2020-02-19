# Show Labels
gam user USER@Domain show labels

# Rename a Label
gam user USER@Domain update labelsettings Contacts name Contacts_1

gam csv Duplicate_Contacts_Label.txt gam user ~Email update labelsettings Contacts name Contacts_1 > LabelRename.csv
