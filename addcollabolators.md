# add_collabolators

*./lib/teachers_pet/actions/add_collabolators.rb*

####Description
Give collaborator access to each provided user.

####Command line
```bash
teachers_pet add_collabolators --repository=[repository] --members=[members] --dryrun=[dryrun]
```
####Descriptions of parameters

[repository] : 'OWNER/REPO'

[members] : 'PATH'.

The path to the file containing the list of usernames to add.

[dry_run] : boolean (optional parameter).

Defaut: false.