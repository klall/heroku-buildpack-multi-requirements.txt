# Heroku buildpack for multiple requirements.txt files

Heroku applications assume one repo to one application.

Given a single repo with multiple applications in it, this buildpack provides the ability to specify a requirements.txt file for each application.

# Usage

1. Create a REQUIREMENTS_TXT.txt file for each application in your repo
2. Create a bunch of Heroku apps.
3. For each app, set `REQUIREMENTS_TXT=relative_path_to_package/requirements.txt` 

4. Add the buildpack from the command line or via the UI
   `heroku buildpacks:add -a <app> https://github.com/klall/heroku-buildpack-multi-requirements.txt`
4. For each app, `git push git@heroku.com:<app> master`
