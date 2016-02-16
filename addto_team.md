# add_to_team

*./lib/teachers_pet/actions/add_tp_team.rb*

####Description
Add members to a Organization.
Adds each user in the list to the team specified my the filename. Creates the team on the specified organization if it doesn't already exist.

####Command line
```bash
teachers_pet add_to_team [organization] [members]
```
###Descriptions of parameters

[organization]

[members] : 'PATH'

The path to the file containing the list of members to add. The filename will be used as the name of the team, e.g. `path/to/instructors.csv` will use the 'instructors' team.


