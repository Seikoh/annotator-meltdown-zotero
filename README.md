# annotator-meltdown-zotero
[Zotero](https://www.zotero.org/) citation lookup for [annotator-meltdown](https://github.com/emory-lits-labs/annotator-meltdown) Annotator.js.

Annotator-Meltdown-Zotero is developed for
[Annotator 2.x](https://github.com/openannotation/annotator/releases)
and is meant to be used with [annotator-meltdown](https://github.com/emory-lits-labs/annotator-meltdown).

##Demo
[View a simple demo of Annotator-Meltdown-Zotero here.](http://emory-lits-labs.github.io/annotator-meltdown-zotero/demo/)

##Dependencies
Depends on [annotator-meltdown](https://github.com/emory-lits-labs/annotator-meltdown) and all of its
[dependencies](https://github.com/emory-lits-labs/annotator-meltdown#dependencies)
* [jquery.rest](https://github.com/jpillora/jquery.rest)
* [bootstrap](http://getbootstrap.com/) for modal window
* [jquery-ui](https://jqueryui.com/) autocomplete

##Using Annotator-Meltdown-Zotero

To use this plugin in your Annotator project, include the required
javascript and css, and initialize it as a viewer and editor extension
within the main annotator ui module.  See
[installation instructions](http://emory-lits-labs.github.io/annotator-meltdown-zotero/#install)
for installation and configuration notes.

## Developer Notes

This project uses [git-flow](https://github.com/nvie/gitflow) branching conventions.

To view the jekyll site for development, you should do the following:
- make sure you are on the **develop** branch
- make sure you have [jekyll installed](http://jekyllrb.com/docs/installation/)
- run the site via jekyll: ```jekyll serve```

To install grunt utilities for building releases, run: ```npm install```

Released versions are published through GitHub site pages, which are served out from
the gh-pages branch.  Following git-flow conventions, this should be an exact
replica of the master branch.  As a convenience, to update the gh-pages branch
from master and push it to github, you may want to configure the following alias
in your ``.git/config`` for this project:

    [alias]
        publish-pages = "!rm -rf build && git checkout gh-pages && git merge master && grunt && git add 'build/*' && git commit 'build/*' -m 'Latest build' && git push origin gh-pages && git checkout -"

Whenever you tag a new release you want to be available as a version that
can be included from the github pages url, you should do the following (or use
the alias above):
- update the version number in package.json
- use gitflow to tag the release
- checkout gh-pages branch, update from master and run ```grunt```
- add the build version of annotator.meltdown.min.js and css to gh-pages branch

