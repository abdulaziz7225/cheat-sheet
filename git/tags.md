# Git Tags

Tags are pointers that refer to particular points in Git history. We can mark a particular moment in time with a tag. Tags are most often used to mark version releases in projects (v4.1.0, v4.1.1, etc.)

- `git tag` – list all tags that exist in this repository
- `git tag -l "*beta*"` – print a list of tags that include `beta` in their name
- `git tag <tag_name> <commit_id>` – tag a specific commit with the given tag name
- `git show <tag_name>` – show which commit the tag refers to
- `git checkout <tag_name>` – open the commit the tag name refers to in a detached HEAD mode
- `git tag -d <tag_name>` – delete the tag with specified name
- `git tag -f <tag_name> <commit_id>` – if we try to reuse a tag that is already referring to a commit, `-f` flag forces to update the tag to another commit

### Pushing Tags

By default, the git push command doesn’t transfer tags to remote servers. If you have a lot of tags that you want to push up at once, you can use the --tags option to the git push command. This will transfer all of your tags to the remote server that are not already there.

- `git push --tags` – push all local tags to remote repository
- `git push origin <tag_name>` – push only the specified tag to remote repository

## Lightweight Tags

### It is simply a pointer to towards a commit in the branch. It points to the latest commit in a specific branch similar to HEAD pointer

- `git tag <tag_name> -m "message"` – create lightweight tag with specified tag name. When commit ID isn't specified, it refers to the latest commit
- `git tag <tag_name> -m "message" <commit_id>` – create lightweight tag with specified tag name. Adding message is optional

## Annotated Tags

### It is a full object in Git. It contains information like the email of the person who added this tag

- `git tag -a <tag_name> -m "message"` – create annotated tag with specified tag name. When commit ID isn't specified, it refers to the latest commit
- `git tag -a <tag_name> -m "message" <commit_id>` – create annotated tag with specified tag name. Adding message is optional
