# Git Submodules

## Add submodule

- `git submodule add <repo-url>`
- `git submodule add <repo-url> <path>` – specify custom folder name

### Example

- `git submodule add https://github.com/user/project.git`
- `git submodule add https://github.com/user/project.git libs/project`

## Clone repo with submodules

- `git clone --recurse-submodules <repo-url>`
- `git submodule update --init --recursive` – if already cloned (initialize + fetch)

## Pull latest changes in submodules

- `git submodule foreach 'git checkout main && git pull origin main'`

## Remove a submodule

- Delete entry in `.gitmodules`
- Delete submodule section from `.git/config`
- Run:

  ```bash
  git rm --cached <path-to-submodule>
  rm -rf <path-to-submodule>
  ```
