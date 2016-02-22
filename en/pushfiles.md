# push_files

*./lib/teachers_pet/actions/push_files.rb*

####Description
Run this command from a local Git repository to push the files up to the specified repository for each student. It will add a remote that is the name of each student team to your repository.

####Command line
```bash
teachers_pet push_files --organization=[organization] --repostitory=[repository] --ssh=[ssh]
```

###Descriptions of parameters

[organization]

[repository]

[ssh] : 'HOST' (Optional parameter)

Default : TeachersPet::Configuration.sshEndpoint

####Oauth parameters
| Parameters |  
| -- | -- |
| --username | (Optional) Default: system username. |
| --pasword = password.| Required the github password of the account. |
| --api = origin| (Optional) The API endpoint of your GitHub Enterprise instance, if you have one. Default: https://api.github.com/|
| --web = origin| (Optional) The URL of your GitHub Enterprise instance, if you have one. Default: https://github.com/ |


 