## Git Tags

### Lightweight Tags

#### It is simply a pointer to towards a commit in the branch. It points to the latest commit in a specific branch similar to HEAD pointer

- `git tag` - lists all tags that exist in this repository
- `git tag <tag_name> <commit_id>` - tag a specific commit with the given tag name
- `git show <tag_name>` - shows which commit the tag refers to
- `git checkout <tag_name>` - opens the commit the tag name refers to in a detached HEAD mode
- `git tag -d <tag_name>` - deletes the tag with specified name

### Annotated Tags

#### It is a full object in Git. It contains information like the email of the person who added this tag

- `git tag -a <tag_name> -m "message"` - creates annotated tag with specified tag name. When commit ID isn't specified, it refers to the latest commit
- `git tag -a <tag_name> -m "message" <commit_id>` - creates annotated tag with specified tag name. Adding message is optional