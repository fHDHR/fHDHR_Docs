# fHDHR.Docs
  
![Doc Deployment](https://github.com/fHDHR/fHDHR_Docs/workflows/Build%20and%20deploy%20docs/badge.svg)

This is the fHDHR Docs site. 
It's not always up-to-date, because our primary developer is a bit of an overachiever.

If you'd like to get involved with the project, reach out in `#fhdhr` over on [Freenode](https://freenode.net/) (and yes, we know IRC is old).

---

## Setting up a dev environment

The easiest method to install mkdocs is via python - it's consistent across different OS environments.  
Install Python for your OS, ensuring that it gets added to PATH.  

Once you have Python installed, you'll need to clone the repository and install the python packages used by this site (like mkdocs itself).
To do this, clone the repo, and from the relevant terminal/shell/prompt, change directory to the repo folder and run  
`pip install -r requirements.txt`  
to ensure you have all the relevant packages for use.

## Editing the site

To edit the site content, edit the markdown files under "docs".  
To edit the site layout, edit the `mkdocs.yml` file (held in the root directory).  

Note that the new documentation repository is not directly publicly editable - for a few reasons, including (but not limited to):

- Markup (as used in `mkdocs.yml`) _is_ an indent-sensitive language.
- Markdown (what all the pages themselves are written with) has defined standards.
- We'd like to be able to validate content _before_ it gets put into official documentation (the old wiki had a lot of inaccurate community-submitted content).

As such, all edit requests will need to go through approval by [submitting a pull request](https://docs.github.com/en/free-pro-team@latest/articles/creating-a-pull-request).

## Suggested editor

[VS Code](https://code.visualstudio.com/) is a good option to use for editing this content, as it has extensions for markup and markdown syntax highlighting (as well as preview functions).  
Included in this repository  is a workspace config for vscode with some defined spelling, linting, and error-checking methods, as well as a group of recommended VS Code extensions for use.  
[Atom](https://atom.io/) is another good option.

## Using mkdocs

The site is being built using [mkdocs](https://www.mkdocs.org/), which converts standard markdown to static html.  
mkdocs itself can be told to 'serve' the folder by opening the folder containing `mkdocs.yml` in your relevant console/terminal and running `mkdocs serve`.  
This will let you live preview the site in your browser, with changes being updated any time you save an edit to a file.  

### mkdocs references

Source reference:

- [mkdocs wiki](https://github.com/mkdocs/mkdocs/wiki)
- [Material theme](https://squidfunk.github.io/mkdocs-material/setup/setting-up-navigation)

Example Configs

- [https://github.com/GhostWriters/DockSTARTer/blob/master/mkdocs.yml](https://github.com/GhostWriters/DockSTARTer/blob/master/mkdocs.yml)
- [https://github.com/selfhosters/selfhosters.net/blob/master/mkdocs.yml](https://github.com/selfhosters/selfhosters.net/blob/master/mkdocs.yml)
- [https://github.com/pi-hole/docs/blob/master/mkdocs.yml](https://github.com/pi-hole/docs/blob/master/mkdocs.yml)
- [https://github.com/TRaSH-/Guides/blob/master/mkdocs.yml](https://github.com/IronicBadger/pms-wiki/blob/main/mkdocs.yml))
- [https://github.com/IronicBadger/pms-wiki/blob/main/mkdocs.yml](https://github.com/IronicBadger/pms-wiki/blob/main/mkdocs.yml))
