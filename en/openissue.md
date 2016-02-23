# open_issue

*./lib/teachers_pet/actions/open_issue.rb*


####Description
Opens a single issue in each repository in the organization.

####Command line
```bash
teachers_pet open_issue --organization=[organization] --repository=[repository] --title=[title] --body=[body] --labels=[labels] --students
```

###Descriptions of parameters

| Parameteres |  
| -- | -- |
| --organization   | The name of your github organization |
| --repository = Owner/Repo| Name of the assignment repository |
| --title = TITLE | The path to the file containing the issue body (.txt or .md)|
| --body | The path to the file containing the issue body (.txt or .md) |
|--labels = labels| LABEL1, LABEL2 |
| --student |(Optional) The path to the file containing the list of user to add. Default: ./students |
[organization] 


####Oauth parameters
| Parameters |  
| -- | -- |
| --username | (Optional) Default: system username. |
| --pasword = password.| Required the github password of the account. |
| --token =token | Provide a token instead of a username+password to authenticate via OAuth |
| --api = origin| (Optional) The API endpoint of your GitHub Enterprise instance, if you have one. Default: https://api.github.com/|
| --web = origin| (Optional) The URL of your GitHub Enterprise instance, if you have one. Default: https://github.com/ |
