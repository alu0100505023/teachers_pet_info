# create_student_teams

*./lib/teachers_pet/actions/create_student_teams.rb*

*./lib/teachers_pet/cli.rb*

####Description
Create teams for each student (or student group), and a team for all the instructors.

####Command line
```bash
teachers_pet create_student_teams --organization=[organization] --students=[students] --username=[username] --password=[password] --token=[token] --api=[api] --web=[web]
```

###Descriptions of parameters

| Parameteres |  
| -- | -- |
| --organization   | The name of your github organization |
| --students = 'PATH'.| The path to the file containing the list of usernames to add. |

[organization]

[students] : 'PATH' (Optional Parameter)
default : ./students



####Oauth parameters
| Parameters |  
| -- | -- |
| --username | (Optional) Default: system username. |
| --pasword = password.| Required the github password of the account. |
| --api = origin| (Optional) The API endpoint of your GitHub Enterprise instance, if you have one. Default: https://api.github.com/|
| --web = origin| (Optional) The URL of your GitHub Enterprise instance, if you have one. Default: https://github.com/ |



