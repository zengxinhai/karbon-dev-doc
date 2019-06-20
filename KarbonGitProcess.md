# Karbon Git Process

## Code Submitting

We adopt the **fork/pull-request** form of submitting code. Every developer has its own repo forked from the main repo. Developer work on their repo in whatever way they like. The only place to control is on the main repo. Whenever the developer want to merge their code to main repo, he/she should make a **pull request to the develop branch**, and another related developer conducts a **code review before merge**.



## Main Repo Branch Responsibility

There're 3 branches:

- **develop**
- **test**
- **master**

### develop

 develop branch is a **place for developers to merge their daily work**. In principle, developers should **merge their work to develop branch at least once a day**. The **features on this branch is not guaranteed to work properly**. But the benefit of using this branch, is to let developers frequently get the latest work of each other, and avoid 90%+ of conflicts when merging. And it's a good habit to prevent from losing developers' work.

### test

test branch is for UAT(user acceptance test) environment. 

Normally, when a developer **finish a feature on develop branch**, he/she should **make pull request to test branch**. The dev-ops periodically pull changes from this branch to publish to UAT servers. 

In some cases, when need to do bug fix for UAT, developer are **allowed to make pull request directly to test branch from their own repo**.  Just remember to do a rebase for develop branch after that.

### master

master branch is **meant for production-ready code**. It only accepts pull request from test branch, **direct push is strictly forbidden.**

