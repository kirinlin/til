# Sync Forked Upstream

link: [Syncing a fork](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/working-with-forks/syncing-a-fork)

```console
linkirin@arale: AgileVerse$ git config -l
...
remote.origin.url=git@github.ibm.com:linkirin/AgileVerse.git
remote.origin.fetch=+refs/heads/*:refs/remotes/origin/*
branch.master.remote=origin
branch.master.merge=refs/heads/master
linkirin@arale: AgileVerse$ git remote add upstream git@github.ibm.com:OGASAY/AgileVerse.git
linkirin@arale: AgileVerse$ git fetch upstream
...
From github.ibm.com:OGASAY/AgileVerse
 * [new branch]      master     -> upstream/master
 * [new tag]         v5.4.6     -> v5.4.6
linkirin@arale: AgileVerse$ git rebase upstream/master
Successfully rebased and updated refs/heads/master.
linkirin@arale: AgileVerse$ git push
...
To github.ibm.com:linkirin/AgileVerse.git
   a9721b8..fc3a21a  master -> master
linkirin@arale: AgileVerse$ git config -l
...
remote.origin.url=git@github.ibm.com:linkirin/AgileVerse.git
remote.origin.fetch=+refs/heads/*:refs/remotes/origin/*
branch.master.remote=origin
branch.master.merge=refs/heads/master
remote.upstream.url=git@github.ibm.com:OGASAY/AgileVerse.git
remote.upstream.fetch=+refs/heads/*:refs/remotes/upstream/*
```
