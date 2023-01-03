## Martin De Robertson's blog

### Resources
Originally cloned from:
https://github.com/skills/github-pages

Alternate theme (Alembic) "installed" up via:
https://github.com/daviddarnes/alembic
(Just the `_config.yml:remote_theme` bit)

### Administrivia

#### SSH Keys and Pushing to GitHub

GitHub does not allow re-using the same SSH key between accounts. These are the steps I took to get this set up and may need to recreate, in part, on a new machine

* Create a new SSH key (`ssh-keygen ...`), add it to your SSH Agent (`ssh-agent add /path/to/private_key`)
* Add the SSH Key to the GitHub account using the web UI
* Ensure the repo is cloned using the SSH URL, not HTTPS (`git remote set-url origin ...`)
* Set the local checkout's config to use the new SSH key (`git config core.sshCommand "ssh -i /path/to/private_key -F /dev/null"`)
