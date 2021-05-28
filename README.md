About this Repository
--

This Github repository contains two branches.

The files in the *source* branch are used by Hugo, a static site generator, to generate the html files that go to the *main* branch.

How do the files from the *source* branch go to the *main* branch?
This is handled by Github Actions. The details are located in .github/workflows/gh-pages.yml.

Everything that exists in the *main* branch is automatically published using Github Pages. Thus the *main* branch should never be edited directly, as it gets overwritten by every push to the *source* branch.

How to contribute?
--

Just fork this repository, checkout from the *source* branch of your fork to a new branch (for example to *my-cool-feature*). Edit some files. Check your work by running `hugo server -D` in the root directory of your cloned fork. If you are happy with your changes, make a pull request to the *source* branch of this repository.
