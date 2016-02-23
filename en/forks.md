# forks

*./lib/teachers_pet/actions/forks.rb*

####Description
Pull the list of users who have forked a particular repository.

####Command line
```bash
teachers_pet forks --repository=[repository] --output=[output]
```

###Descriptions of parameters


| Parameteres |  
| -- | -- |
| --repository = Owner/Repo| Name of the assignment repository |
| --output = 'PATH' | (Optional) Default: './student.csv' |



####Oauth parameters
| Parameters |  
| -- | -- |
| --username | (Optional) Default: system username. |
| --pasword = password.| Required the github password of the account. |
| --token =token | Provide a token instead of a username+password to authenticate via OAuth |
| --api = origin| (Optional) The API endpoint of your GitHub Enterprise instance, if you have one. Default: https://api.github.com/|
| --web = origin| (Optional) The URL of your GitHub Enterprise instance, if you have one. Default: https://github.com/ |
