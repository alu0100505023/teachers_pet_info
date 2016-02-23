# push_files

*./lib/teachers_pet/actions/push_files.rb*

####Description
Run this command from a local Git repository to push the files up to the specified repository for each student. It will add a remote that is the name of each student team to your repository.

####Command line
```bash
teachers_pet push_files --organization--repostitory --ssh
```

###Descriptions of parameters

| Parameteres |  
| -- | -- |
| --organization   | The name of your github organization |
| --repository = Owner/Repo| Name of the assignment repository |
| --students= 'PATH' |(Optional) The path to the file containing the list of user to add. Default: ./students  |
| --ssh: 'HOST' | (Optional) Default: github.com|


####Oauth parameters
| Parameters |  
| -- | -- |
| --username | (Optional) Default: system username. |
| --pasword = password.| Required the github password of the account. |
| --token =token | Provide a token instead of a username+password to authenticate via OAuth |
| --api = origin| (Optional) The API endpoint of your GitHub Enterprise instance, if you have one. Default: https://api.github.com/|
| --web = origin| (Optional) The URL of your GitHub Enterprise instance, if you have one. Default: https://github.com/ |


 