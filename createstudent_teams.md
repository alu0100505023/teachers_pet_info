# create_student_teams

*./lib/teachers_pet/actions/create_student_teams.rb*

*./lib/teachers_pet/cli.rb*

####Description
Create teams for each student (or student group), and a team for all the instructors.

####Command line
```bash
teachers_pet create_student_teams --organization=[organization] --students=[students] --username=[username] --password=[password] --token=[token] --api=[api] --web=[web]
```

###Descriptions of parameters
[organization]

[students] : 'PATH' (Optional Parameter)
default : ./students

[username] (Optional parameter)
default : system name.

[password] (Optional parameter)

[token] : token (Optional parameter)

Provide a token instead of a username+password to authenticate via OAuth. See https://github.com/education/teachers_pet#authentication.

[api] : Origin (Optional parameter)
The API endpoint of your GitHub Enterprise instance, if you have one.

Default: https://api.github.com/ 

[web] : Origin (Optional parameter)
The URL of your GitHub Enterprise instance, if you have one.

Default: https://github.com/



