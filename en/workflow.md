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

### Giving others access

You may need to give other people access to various repositories using teams – the `add_to_team` command can help do this in bulk.

### Creating assignments

When using the [sandboxing](https://education.github.com/guide/sandboxing) setup, you will need to create the repositories for the students.  For each assignment, use the `create_repos` action to create a repository for each student.  The repositories are technically created per team, but if you use `create_student_teams` first, then there will be one team per student.

### Forks

If you need to grab the list of users who have forked a particular repository – e.g. to use with another command – you can run the `forks` command, and the results will be written to a file.

### Collaborator access

Give [collaborator access](https://help.github.com/articles/what-are-the-different-access-permissions#collaborator) to everyone who has forked your repository using `add_collaborators`.  Mostly useful for GitHub demonstrations, where usernames can quickly be collected via `forks`, and then the students can be quickly given access to a repository.

### Pushing starter files

When creating repositories for students, you will often want to include boilerplate files.  After running `create_repos`, create a canonical copy of the starter files (e.g. [`.gitignore`](https://github.com/github/gitignore#readme), `Makefile`s, etc.) in a repository.  From the local clone of the repository, use the `push_files` action to place that code in the repositories for each student.  This works by creating a Git remote for each student repository, and doing a `git push` to each one.

### Opening issues

After running `create_repos`, instructors can open issues in student repos as a way to list requirements of the assignment, goals, or instructions for patching, using the `open_issue` command.

### Clone repositories for grading

When grading, use the `clone_repos` command to clone all the repositories in the organization that match the username-repository naming scheme that is generated when `create_repos` is run.

### Merge all open pull requests

When running a GitHub workshop, it's nice to be able to merge a bunch of pull requests on a particular repository all at once. `merge_pull_requests` will handle this for you.
