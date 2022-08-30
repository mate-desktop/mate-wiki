## MATE Wiki

This repository holds the source files for the MATE Wiki: https://wiki.mate-desktop.org/

The files in the *master* branch are used by Hugo, a static site generator, to generate the html files that go to the *gh-pages* branch.

How do the files from the *master* branch go to the *gh-pages* branch?
This is handled by Github Actions. The details are located in .github/workflows/.

Everything that exists in the *gh-pages* branch is automatically published using Github Pages. Thus the *gh-pages* branch should never be edited directly, as it gets overwritten by every push to the *master* branch.

### How to contribute?

Just fork this repository, checkout from the *master* branch of your fork to a new branch (for example to *my-cool-feature*). Edit some files. Check your work by running `hugo server -D` in the root directory of your cloned fork. If you are happy with your changes, make a pull request to the *master* branch of this repository.

Or, even easier click the *Edit this page* button on the top hand right side of each webpage and follow Githubs instructions to edit the page directly in your webbrowser.

### Helpful resources
 - https://gohugo.io/ (Hugo Official Website)
 - https://github.com/peaceiris/actions-hugo (Hugo Github Actions)
 - https://geekdocs.de/ (Theme)
