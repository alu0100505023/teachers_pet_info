# clone_repos

*./lib/teachers_pet/actions/clone_repos.rb*

####Description
Clone all student repositories for a particular assignment into the current directory.

####Command line
```bash
teachers_pet clone_repos --organization=[organization] --repository=[repository] --clone_method=[clone_method]
```
###Descriptions of parameters

[organization]

[repository]

[clone_method] : 'Option' (Optional parameter).

Option: 'https' or 'ssh'. Default: 'https'.

####Oauth parameters
| Parameters |  
| -- | -- |
| --username | (Optional) Default: system username. |
| --pasword = password.| Required the github password of the account. |
| --api = origin| (Optional) The API endpoint of your GitHub Enterprise instance, if you have one. Default: https://api.github.com/|
| --web = origin| (Optional) The URL of your GitHub Enterprise instance, if you have one. Default: https://github.com/ |


