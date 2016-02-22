# clone_repos

*./lib/teachers_pet/actions/clone_repos.rb*

####Description
Clone all student repositories for a particular assignment into the current directory.

####Command line
```bash
teachers_pet clone_repos --organization --repository --clone_method
```
###Descriptions of parameters

| Parameteres |  
| -- | -- |
| --organization   | The name of your github organization |
| --repository = Owner/Repo| Name of the assignment repository |
|  --clone_method | (Optional) 'https' or 'ssh'. Default: 'https'.  |


####Oauth parameters
| Parameters |  
| -- | -- |
| --username | (Optional) Default: system username. |
| --pasword = password.| Required the github password of the account. |
| --api = origin| (Optional) The API endpoint of your GitHub Enterprise instance, if you have one. Default: https://api.github.com/|
| --web = origin| (Optional) The URL of your GitHub Enterprise instance, if you have one. Default: https://github.com/ |


