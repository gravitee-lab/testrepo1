# The Gravitee Release Orchestrator

This markdown file is a utility I use to quickly resume work on my last task, on this repo.

Change this for yoru own needs when you fork this repo.

# To resume work

* copy/paster :

```bash

git config --global commit.gpgsign true
git config --global user.name "Jean-Baptiste-Lasselle"
git config --global user.email jean.baptiste.lasselle.pegasus@gmail.com
git config --global user.signingkey 7B19A8E1574C2883

git config --global --list

# will re-define the default identity in use
# https://docstore.mik.ua/orelly/networking_2ndEd/ssh/ch06_04.htm
ssh-add ~/.ssh.perso.backed/id_rsa

export GIT_SSH_COMMAND='ssh -i ~/.ssh.perso.backed/id_rsa'
ssh -Ti ~/.ssh.perso.backed/id_rsa git@github.com


export LOCAL_WORKSPACE=~/testrepo1
cd ${LOCAL_WORKSPACE}
export FEATURE_ALIAS="orbs-tests"
export COMMIT_MESSAGE="feat.(${FEATURE_ALIAS}): testing orb [ccc],  working on https://github.com/gravitee-io/release/issues/145"
# git add --all && git commit -m "${COMMIT_MESSAGE}" && git push -u origin HEAD
atom .

```
