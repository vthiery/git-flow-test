# How to ... #

## ... get ready? ##
Go to https://github.com/petervanderdoes/gitflow-avh/wiki and read carefully.

## ... start using git-flow in an existing repo? ##
Simply run
```
git flow init
```
and make sure to comply with the existing style of prefixes if any.

## ... start working on a feature? ##
In order to start a feature, you can
```
git flow feature start feature-name
```
and start committing as usual. When your feature is ready, simply
```
git flow feature publish feature-name
```
and open a pull request. When approved, do not merge as usual but use
```
git flow feature finish feature-name
```
such that the feature is merged into 'develop' and closed afterwards.

## ... pull a feature from another branch? ##
Just do
```
git flow feature pull other-feature-name
```
and you are done.

## ... release in master? ##
Let's say you want to release a version from 0.1.0, then do
```
git flow release start 0.2.0
```
assuming the second number is the standard release counter.
Any fixes to be done on the release branch are done as usual. Then publish with
```
git flow release publish 0.2.0
```
and when approved, release with
```
git flow release finish 0.2.0
```

## ... release a hotfix? ##
Create a hotfix branch with
```
git flow hotfix start 0.2.1
```
assuming the last number is the patch counter. Commit as usual, and then
```
git flow hotfix publish 0.2.1
```
and open a pull request.
Then simply
```
git flow hotfix finish 0.2.1
```

