---
title: Tips & Tricks
weight: -15
---

In this section all developers can share useful hints and small scripts which aid in the development process. You might also want to look at the [MATE Development Scripts](https://github.com/mate-desktop/mate-dev-scripts) at Github.

{{< toc >}}

<!--Please keep this list alphabetically sorted-->

## Git

**Goal**: *Exclude translation commits in [gitk](https://git-scm.com/docs/gitk)'s log*

**How to**:
 1. Run `gitk --perl-regexp` in the project folder
 2. Go to `View->Edit View`
 3. Type `^[translation]` in the Commit Message field
 4. Apply the changes

**More info**: https://stackoverflow.com/a/39794232

