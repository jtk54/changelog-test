Notes on Conventional-Changelog (vanilla cli) [ ]
=============================================

Using Conventional-Changelog
----------------------------

* Sample usage: https://github.com/conventional-changelog/conventional-changelog-cli.
* Workflow goes like: https://github.com/conventional-changelog/conventional-changelog-cli#recommended-workflow.
* Commit tags defined here: https://github.com/conventional-changelog/conventional-changelog/blob/a5505865ff3dd710cf757f50530e73ef0ca641da/conventions/angular.md
* Commit tags also defined here: https://github.com/conventional-changelog/conventional-changelog-angular/blob/master/index.js#L50.

Dependencies and Issues
-----------------------

* Seems to be a dependency on `npm` here, even for the groovy projects. (issue)
* Requires a package.json to determine the latest version in the changelog. Does a diff based on semver tags.
* We'd need a minimal package.json for each compoment. (issue)
* Can't filter out alternative tags. This means Netflix's tags will show up in the generated product changelogs. We can clean this up for a product release. Or not. (issue)
* Very useful and flexible command line tool. Uses git metadata only, not github.
* Would be great and simple to use if we had one tag flavor, or could filter the diffs on tags.


Notes on clog [x]
=============

Using clog
----------

* Sample usage: https://github.com/clog-tool/clog-cli#using-clog-from-the-command-line
* Commit tags defined here: https://github.com/conventional-changelog/conventional-changelog/blob/a5505865ff3dd710cf757f50530e73ef0ca641da/conventions/angular.md

Dependencies, Notes and Issues
------------------------------

* Follows same commit structure as (angular) conventional-changelog.
* Dependencies on rust and cargo (rust package manager).
* `npm` distribution for mac only.
* Diff based on commit ranges. Doesn't care about semver tags at all.
* Can use `git show-ref --tags` and filter to grab relevant commits only.
* Can label a changelog with an arbitrary version. Doesn't require package.json or anything.
* Very useful and flexible command line tool. Uses git metadata only, not github.
