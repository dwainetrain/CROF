Sometimes there's conflicts with yarn.lock and the git branch. Here's the process to solve them:
First commit the branch you're working on
Then switch to master and attempt to merge the dev branch in
You should get a conflict error
git checkout --theirs package.json (you're checkout out dev's files)
git checkout --theirs yarn.lock
yarn or yarn install
add files and commit
