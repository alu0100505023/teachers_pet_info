# create_repos

*./lib/teachers_pet/actions/create_repos.rb*

####Description
"Create assignment repositories for students

####Command line
```bash
teachers_pet create_repos --organization=[organization] --repository=[repository] --public=[public]
```
###Descriptions of parameters
[organization]

[repository]

[public] : boolean (Optional parameter).

"Make the repositories public". Default : false.

[--no-public]

[--students=PATH] 

####Oauth parameters
| Parameters |  
| -- | -- |
| --username | (Optional) Default: system username. |
| --pasword = password.| Required the github password of the account. |
| --token =token | Provide a token instead of a username+password to authenticate via OAuth |
| --api = origin| (Optional) The API endpoint of your GitHub Enterprise instance, if you have one. Default: https://api.github.com/|
| --web = origin| (Optional) The URL of your GitHub Enterprise instance, if you have one. Default: https://github.com/ |
