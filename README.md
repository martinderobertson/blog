## Martin De Robertson's blog

### Resources, or How To Add New Content
Originally cloned from:
https://github.com/skills/github-pages

Alternate "theme" (`Minimal Mistakes`) "installed" via:
* https://mmistakes.github.io/minimal-mistakes/docs/configuration/

(Note that "theme" here means way more than just the colors and layout. Basically any new page or element or asset or whatever should be through this)

New content isn't limited to just blog posts. See here for additional types of pages this theme can make
https://github.com/mmistakes/minimal-mistakes

### Testing

Local testing _should_ be achievable. I think macOS comes with too low of a Ruby version or something. I think the work I did for that is on the `new-jekyll-theme-alembic-2` branch; this included something like figuring out how to install `nokogiri` and some other bullshit

Pro tip: `bundle exec ...` is a nice convenient shortcut through doing things through the Ruby bundler, like `npm` or `venv` or whatever the hell.

### Administrivia

#### SSH Keys and Pushing to GitHub

GitHub does not allow re-using the same SSH key between accounts. These are the steps I took to get this set up and may need to recreate, in part, on a new machine

* Create a new SSH key (`ssh-keygen ...`), add it to your SSH Agent (`ssh-agent add /path/to/private_key`)
* Add the SSH Key to the GitHub account using the web UI
* Ensure the repo is cloned using the SSH URL, not HTTPS (`git remote set-url origin ...`)
* Set the local checkout's config to use the new SSH key (`git config core.sshCommand "ssh -i /path/to/private_key -F /dev/null"`)
