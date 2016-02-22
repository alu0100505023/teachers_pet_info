# forks

*./lib/teachers_pet/actions/forks.rb*

####Description
Pull the list of users who have forked a particular repository.

####Command line
```bash
teachers_pet forks --repository=[repository] --output=[output]
```

###Descriptions of parameters


[repository] : 'OWNER/REPO'

[output] : 'PATH' (Optional parameter)

Default: 'students.csv'

####Oauth parameters
| Parameters |  
| -- | -- |
| --username | (Optional) Default: system username. |
| --pasword = password.| Required the github password of the account. |
| --api = origin| (Optional) The API endpoint of your GitHub Enterprise instance, if you have one. Default: https://api.github.com/|
| --web = origin| (Optional) The URL of your GitHub Enterprise instance, if you have one. Default: https://github.com/ |
