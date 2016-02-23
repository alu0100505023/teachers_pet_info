# create_repos

*./lib/teachers_pet/actions/create_repos.rb*

####Description
"Create assignment repositories for students

####Command line
```bash
teachers_pet create_repos --organization --repository --students --public
```
###Descriptions of parameters

| Parameteres |  
| -- | -- |
| --organization   | The name of your github organization |
| --repository='Owner/Repo' |Name of the assignment repository |
| --students = 'PATH'.| (Optional) The path to the file containing the list of user to add. Default: ./students |
|--public = boolean |(Optional) Default: False| 
|--no-public| (Optional) Default: True   | 



####Oauth parameters
| Parameters |  
| -- | -- |
| --username | (Optional) Default: system username. |
| --pasword = password.| Required the github password of the account. |
| --token =token | Provide a token instead of a username+password to authenticate via OAuth |
| --api = origin| (Optional) The API endpoint of your GitHub Enterprise instance, if you have one. Default: https://api.github.com/|
| --web = origin| (Optional) The URL of your GitHub Enterprise instance, if you have one. Default: https://github.com/ |
