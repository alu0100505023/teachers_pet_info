# open_issue

*./lib/teachers_pet/actions/open_issue.rb*


####Description
Opens a single issue in each repository in the organization.

####Command line
```bash
teachers_pet open_issue --organization=[organization] --repository=[repository] --title=[title] --body=[body] --labels=[labels]
```

###Descriptions of parameters
[organization] 

[repository]

[title] : 'title' (Optional parameter)

The title of the issue to be created

[body] : 'PATH' (Optional parameter)

The path to the file containing the issue body (.txt or .md)

[labels] : 'label' (Optional parameter)

label: LABEL1,LABEL2

####Oauth parameters
| Parameters |  
| -- | -- |
| --username | (Optional) Default: system username. |
| --pasword = password.| Required the github password of the account. |
| --api = origin| (Optional) The API endpoint of your GitHub Enterprise instance, if you have one. Default: https://api.github.com/|
| --web = origin| (Optional) The URL of your GitHub Enterprise instance, if you have one. Default: https://github.com/ |
