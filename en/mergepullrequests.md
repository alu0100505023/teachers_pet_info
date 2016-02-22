# merge_pull_requests

*./lib/teachers_pet/actions/merge_pull_requests.rb*



####Description
Merges all open pull requests on a particular repository

####Command line
```bash
teachers_pet merge_pull_requests --repository=[repository]
```

###Descriptions of parameters
[repository] : 'OWNER/REPO'

####Oauth parameters
| Parameters |  
| -- | -- |
| --username | (Optional) Default: system username. |
| --pasword = password.| Required the github password of the account. |
| --token =token | Provide a token instead of a username+password to authenticate via OAuth |
| --api = origin| (Optional) The API endpoint of your GitHub Enterprise instance, if you have one. Default: https://api.github.com/|
| --web = origin| (Optional) The URL of your GitHub Enterprise instance, if you have one. Default: https://github.com/ |
