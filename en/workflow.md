# Workflow

## Typical workflow

...when using the [sandboxing](https://education.github.com/guide/sandboxing) method with [private repositories](https://education.github.com/guide/private_repos):

### Basic setup

1. Create an organization (you will be an owner by default). The organization should reflect the name of your course. See [the classroom guide](https://education.github.com/guide#2-create-an-organization-for-your-class) for more info.
1. Have each student/instructor create GitHub accounts.
1. Create a `students` file (you can use an alternate filename and specify with the `--students` option if you like)
    * Individual assignments: one username per line
    * Group assignments: one team per line in the format `teamName username username username`
1. Add the GitHub username of all instructors to an `Owners.csv` file (one per line)
1. Run the following:

    ```bash
    teachers_pet create_student_teams ...
    teachers_pet add_to_team --members Owners.csv ...
    ```

### Assignments

```bash
teachers_pet create_repos ...
teachers_pet push_files ...
# Multiple times:
teachers_pet open_issue ...

# Then, after the assignment is due,
teachers_pet clone_repos ...
```

