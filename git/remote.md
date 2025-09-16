# Git Remote

Before we can push anything up to Github, we need to tell Git about our remote repository on Github. We need to setup a "destination" to push up to. In Git, we refer to these "destinations" as remotes. Each remote is simply a URL where a hosted repository lives.

- `git remote add <name> <url>` – add the specified `<url>` and refer to it with the `<name>` ("origin" is convention)
- `git remote -v` – show the remote repository in case there is any, -v flag stands for verbose
- `git remote rename <old_name> <new_name>` – rename the repository with a new name
- `git remote remove <name>` – delete remote repository if needed
- `git remote set-url origin <url>` – update the remote url
- `git remote add upstream <forked_repository>` – add `<forked_repository>` as `upstream` to pull latest changes
