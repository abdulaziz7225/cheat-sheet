# Git Aliases

We can easily set up Git aliases to make our Git experience a bit simpler and faster. For example, we could define an alias `git ci` instead of having to type `git commit`. Also, we could define a custom `git lg` command that prints out a custom formatted commit log.

- `git config --global alias.<alias_name> <git_command>` – set the alias from the command line

## Must-have aliases to print out the history in a pretty format

```bash
[alias]
ls = log --pretty=format:"%C(yellow)%h%Cred%d\\ %Creset%s%Cblue\\ [%cn]" --decorate
ll = log --pretty=format:"%C(yellow)%h%Cred%d\\ %Creset%s%Cblue\\ [%cn]" --decorate --numstat
```
