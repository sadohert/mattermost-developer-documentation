---
title: "Mattermost tick-tock Branching Strategy"
date: 2019-06-18T00:00:00-04:00
subsection: Getting Started
---

Mattermost uses a [tick-tock release strategy](https://docs.mattermost.com/process/release-faq.html#release-overview) where every other release is a "quality release" that only has bug fixes and no new features.

The following diagram provides an overview of the branching strategy used to accomplish this. As an example, release-5.4 is a feature release and release-5.5 is a quality release. Note the "quality release" branch is based on the previous release branch.

![Branching Overview](/contribute/getting-started/branching-overview.png)


## Cherry Pick Process - Developer

When your PR is required on a release branch, you will follow the cherry picking process.

1. Make a PR to 'master' like normal.
1. Add the appropriate milestone and the `CherryPick/Approved` label.
1. When your PR is approved, it will be assigned back to you to perform the merge and any cherry picking if necessary.
1. Merge the PR.
1. Cherry pick the master commit back to the appropriate releases. If the release branches have not been cut yet, leave the labels as-is and cherry-pick once the branch has been cut. The release manager will remind you to finish your cherry-pick.
1. Set the `CherryPick/Done` label when completed.


## Cherry Pick Process - Reviewer

If you are the second reviewer reviewing a PR that needs to be cherry-picked, do not merge the PR. If the submitter is a core team member, you should set the `Reviews Complete` label and assign it to the submitter to cherry pick. If the submitter is a community member who is not available to cherry pick their PR or can not do it themselves, you should follow the cherry pick process above.
