# Karbon Git Process

## Code Submitting

We adopt the **fork/pull-request** form of submitting code. Every developer has its own repo forked from the main repo. Developer work on their repo in whatever way they like. The only place to control is on the main repo. Whenever the developer want to merge their code to main repo, he/she should make a **pull request to the corresponding feature branch**, and another related developer conducts a **code review before merge**.

## Main Repo Branch Responsibility

### Fixed Branches

There're 3 fixed branches:

- **sit**
- **uat**
- **master**

#### sit

This branch is for SIT(system integration testing).

Normally, when developer **finish a feature on feature branch**, he/she should **make pull request to sit branch**.

#### uat

This branch is for UAT(user acceptance testing).

When a feature passes SIT test, it will be merged to this branch. The tester should start testing after a new feature has been merged.

The dev-ops periodically pull changes from this branch to publish to UAT servers.

#### master

master branch is **meant for production-ready code**.

It only accepts pull request from uat branch, **direct push is strictly forbidden.**

### Feature Branches

Feature branch is a **place for developers to merge their daily work**.

In principle, developers should **merge their work to corresponding feature branch at least once a day**. The **feature on these branches are not guaranteed to work properly**.

The benefit of frequent merge, is to let developers frequently get the latest work of each other, and avoid 90%+ of conflicts when merging. And it's a good habit to prevent from losing developers' work.
