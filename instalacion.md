# Installation



[Install Ruby 1.9.3+](https://www.ruby-lang.org/en/installation/), (recommended 2.3.0) then run

```bash
gem install teachers_pet
```
Or if you want to use bundle:
```bash
bundle install teachers_pet
```
If you've used this tool before, get the newest version using

```ruby
gem update teachers_pet
```

Modify *lib/teachers_pet/configuration.rb* to add the specific information of your application. 


## Authentication

The scripts will ask for your GitHub password in order to run. If you have [two factor authentication](https://help.github.com/articles/about-two-factor-authentication) (2FA) enabled, [create a personal access token](https://help.github.com/articles/creating-an-access-token-for-command-line-use) (replace `github.com` with your host for GitHub Enterprise):

https://github.com/settings/tokens/new?description=teachers_pet&scopes=repo%2Cpublic_repo%2Cwrite%3Aorg%2Crepo%3Astatus%2Cread%3Aorg%2Cuser%2Cadmin%3Aorg

Once created, specify the token using the `--token` option, or if you add the `TEACHERS_PET_GITHUB_TOKEN` environment variable to your `.bash_profile` (or equivalent – example below), it will be picked up by `teachers_pet`.

```bash
# replace YOUR_TOKEN_HERE below
echo "\n\nexport TEACHERS_PET_GITHUB_TOKEN=YOUR_TOKEN_HERE" >> ~/.bash_profile
source ~/.bash_profile
```