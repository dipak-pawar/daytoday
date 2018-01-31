
##### How to pull upstream PR locally?
* Open .git/config
* Change
  ```
  [remote "upstream"]
    url = https://github.com/arquillian/smart-testing
    fetch = +refs/heads/*:refs/remotes/upstream/*
  ```
  To
  ```
  [remote "upstream"]
    url = https://github.com/arquillian/smart-testing
    fetch = +refs/heads/*:refs/remotes/upstream/*
    fetch = +refs/pull/*/head:refs/remotes/upstream/pr/*
  ```
* Fetch all PR's using  `git fetch origin`
* Fetch single PR using `git fetch origin pull/ID/head:BRANCHNAME` e.g.`git fetch upstream pull/227/head:fix-asertions`
