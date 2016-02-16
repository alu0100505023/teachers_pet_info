# open_issue

*./lib/teachers_pet/actions/open_issue.rb*


####Description
Opens a single issue in each repository in the organization.

####Command line
```bash
teachers_pet merge_pull_requests [repository]
```

###Descriptions of parameters
[repository] : 'OWNER/REPO'


option :organization, required: true
1     option :repository, required: true
1     option :title, desc: "The title of the issue to be created"
1     option :body, banner: 'PATH', desc: "The path to the file containing the issue body (.txt or .md)"
1     option :labels, banner: 'LABEL1,LABEL2'
