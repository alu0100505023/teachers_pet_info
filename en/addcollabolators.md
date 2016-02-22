# add_collabolators

*./lib/teachers_pet/actions/add_collabolators.rb*

####Description
Give collaborator access to each provided user.

####Command line
```bash
teachers_pet add_collabolators --repository --members --dryrun
```
####Descriptions of parameters

| Parameter |  
| -- | -- |
| --repository = Owner/Repository | -- |
| --members = 'PATH'.| The path to the file containing the list of usernames to add. |
| --dry_run = boolean| (Optional) Defaut: false. |


####Oauth parameters
| Parameters |  
| -- | -- |
| --username | (Optional) Default: system username. |
| --pasword = password.| Required the github password of the account. |
| --api = origin| (Optional) The API endpoint of your GitHub Enterprise instance, if you have one. Default: https://api.github.com/|
| --web = origin| (Optional) The URL of your GitHub Enterprise instance, if you have one. Default: https://github.com/ |






