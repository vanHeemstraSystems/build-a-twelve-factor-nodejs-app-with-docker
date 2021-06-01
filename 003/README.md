# 003. Use Git Flow as a Reliable Version Control Model

Video: https://egghead.io/lessons/git-use-git-flow-as-a-reliable-version-control-model

A reliable version control and source code tracking process is important for delivering apps with consistency and reliability. In this lesson, we will learn aspects of the Git Flow branching model which provide standards for developing and deploying apps with Git. We will walk through the methodologies of this well-known branching model, how to work with it from develop through to staging environments, and versioning your source code properly for production.

Transcript

Instructor: 00:00 Git flow is a branching model for Git well suited for scaling a development team. Let's create a new repository. New repositories are created by default with a master branch and no commits. Let's go ahead and create a new read me file, add it to a repo, and commit it to kick things off. We'll also add a remote origin from GitHub and push our initial commit upstream.

00:26 The develop branch always contains completed features and fixes. Therefore, it is considered the working tree for our source repository. Go ahead and create a new develop branch and push it upstream.

00:42 All new development is built within a feature branch. Feature branches are always branched off of the develop branch and prefixed with a feature slash. All work within this feature is now completed within the foo branch. Do your work and commit like usual.

01:02 Let's create another feature, this time named bar. Keeping feature branches separate keeps all commits related to a specific task or feature isolated. When you're complete with your feature, it is merged back into the develop branch.

01:21 This is usually accomplished with a pull request so it can pass through a proper code review by another peer, but for now, we will just merge this feature back into the develop manually. It is a good idea to do a Git pull on the develop branch often to refresh your local working tree from the remote origin.

01:40 Since we just created a repo, there won't be any updates to pull down. You will want to rebase your branch from develop if you believe updates from a remote origin could potentially cause conflicts with your changes or if you just wanted to pull down the latest updates from develop.

01:57 If you check the log of the feature/bar branch, you will see that this branch has just the new bar.js file. Let's rebase from develop. This will rewind your feature branch, apply the updates from develop, and then replay your commits on top of the last commit. We can verify this by checking the logs again and see that the new foo.js file has been placed before our new bar.js file commit.

02:24 Let's go ahead and merge our features/bar branch into develop and then push it upstream. It looks like our code is now ready for release, so we will create a new release branch. Every release branch contains the release version, in this case, 1.0Since the release is in its own branch, we don't have to worry about updates from develop conflicting with a specific release. We can now push this upstream and deploy the code to a staging environment for testing.

02:58 Let's say our QA team did some testing and the foo text is actually supposed to be outputted twice. Let's update our foo.js file. We will then go ahead and commit this directly to the release branch. If you were working with a larger team, you can also create a new feature branch and submit a pull request to the release branch.

03:21 We'll push the release repository upstream and repeat the process until our release branch has passed into a testing phase on staging and is ready to be released to production. When the updates to this release are complete, the release branch is merged back into develop as we want to make sure any updates or bug fixes that were applied in our release testing are merged back into the working tree.

03:45 Since the code in the release branch is fully tested and ready to be released to production, we also want to merge it into our master branch which should only ever contain production ready code. Then we tag the release. We can then push the tag upstream and then use that tag to deploy our code to production.

04:03 The only commits to master are merges from either a release branch or a hot fix branch. Hot fixes are intended only for emergency fixes and follow a similar format to feature branches, prefixed with a hot fix slash.

04:19 Note that hot fixes branch from master. We then merge the hot fix back in the master. Then tag and push our new release. We also want the hot fix to be applied back into our develop branch so it's not lost with the future updates.

04:39 When releases are complete, it's usually good practice to delete all previously merged in branches. If we're following a pull request model, you can remove these at the time of the merger pull request acceptance. Otherwise, you can just manually remove these branches locally and remotely.


