# Ansible Role: Dotfiles


Installs a set of dotfiles from a given Git repository.

## Requirements

Requires `git` on the managed machine (you can easily install it with `geerlingguy.git` if required).

## Role Variables
```yml
dotfile_user:
  - username: daniel
    dotfiles_repo: "https://github.com/DanielMueller1309/dotfiles.git"
    dotfiles_repo_version: master
    dotfiles_repo_accept_hostkey: false
    dotfiles_repo_local_destination: "/home/daniel/Git/dotfiles"
    dotfiles_home: "/home/daniel"
    dotfiles_files:
      - .bashrc
      - .tmux.conf
      - .gitignore
      - .vimrc
```
## Example Playbook

    - hosts: localhost
      roles:
        - { role: DanielMueller1309.dotfiles_multiuser become:true }

## License
MIT / BSD

