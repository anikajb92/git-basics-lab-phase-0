Last login: Fri Feb 26 19:58:02 on ttys001
anikabernstein@anikas-imac ~ % git clone git@github.com:anikajb92/git-basics-lab-phase-0.git
Cloning into 'git-basics-lab-phase-0'...
Warning: Permanently added the RSA host key for IP address '140.82.112.4' to the list of known hosts.
remote: Enumerating objects: 170, done.
remote: Total 170 (delta 0), reused 0 (delta 0), pack-reused 170
Receiving objects: 100% (170/170), 52.95 KiB | 444.00 KiB/s, done.
Resolving deltas: 100% (91/91), done.
anikabernstein@anikas-imac ~ % cd git-basics-lab-phase-0
anikabernstein@anikas-imac git-basics-lab-phase-0 % npm install

added 201 packages, and audited 202 packages in 2s

4 low severity vulnerabilities

To address all issues, run:
  npm audit fix

Run `npm audit` for details.
anikabernstein@anikas-imac git-basics-lab-phase-0 % npm test

> git-basics-lab@1.0.0 test
> mocha --timeout 5000 -R mocha-multi --reporter-options spec=-,json=.results.json



  this lab
    1) has a folder named my-repository
    2) has a valid git repository initialized for the my-repository folder
    3) has a README.md file in the my-repository folder

  the local repository
    4) has README.md as a tracked file
    5) has at least one commit
    6) has been pushed up to the remote repository


  0 passing (8ms)
  6 failing

  1) this lab
       has a folder named my-repository:
     AssertionError: no folder name "my-repository" was found: value: expected './my-repository' to exist
      at Function.<anonymous> (node_modules/chai-fs/lib/assertions/directory.js:21:53)
      at Function.ctx.<computed> [as directory] (node_modules/chai/lib/chai/utils/addMethod.js:41:25)
      at Function.assert.isDirectory (node_modules/chai-fs/lib/assertions/directory.js:34:35)
      at Context.<anonymous> (test/index-test.js:9:17)
      at processImmediate (node:internal/timers:464:21)

  2) this lab
       has a valid git repository initialized for the my-repository folder:
     AssertionError: no ".git" folder was found within "/my-repository, used "git init" to initialize: value: expected './my-repository/.git' to exist
      at Function.<anonymous> (node_modules/chai-fs/lib/assertions/directory.js:21:53)
      at Function.ctx.<computed> [as directory] (node_modules/chai/lib/chai/utils/addMethod.js:41:25)
      at Function.assert.isDirectory (node_modules/chai-fs/lib/assertions/directory.js:34:35)
      at Context.<anonymous> (test/index-test.js:13:17)
      at processImmediate (node:internal/timers:464:21)

  3) this lab
       has a README.md file in the my-repository folder:
     AssertionError: no README.md file found within "/my-repository": expected './my-repository/README.md' to exist
      at Function.assert.pathExists (node_modules/chai-fs/lib/assertions/path.js:31:35)
      at Context.<anonymous> (test/index-test.js:17:17)
      at processImmediate (node:internal/timers:464:21)

  4) the local repository
       has README.md as a tracked file:
     AssertionError: no files are being tracked.  Use "git add ." to track all files in this repo: expected './my-repository/.git/index' to exist
      at Function.assert.pathExists (node_modules/chai-fs/lib/assertions/path.js:31:35)
      at Context.<anonymous> (test/index-test.js:25:17)
      at processImmediate (node:internal/timers:464:21)

  5) the local repository
       has at least one commit:
     AssertionError: no commits were found.  Use "git commit -m" followed by a message to create a commit: value: expected './my-repository/.git/logs' to exist
      at Function.<anonymous> (node_modules/chai-fs/lib/assertions/directory.js:21:53)
      at Function.ctx.<computed> [as directory] (node_modules/chai/lib/chai/utils/addMethod.js:41:25)
      at Function.assert.isDirectory (node_modules/chai-fs/lib/assertions/directory.js:34:35)
      at Context.<anonymous> (test/index-test.js:29:17)
      at processImmediate (node:internal/timers:464:21)

  6) the local repository
       has been pushed up to the remote repository:
     AssertionError: no record of pushing to a remote was found. Follow the instructions on GitHub to connect and push to a new remote repository: value: expected './my-repository/.git/logs/refs/remotes' to exist
      at Function.<anonymous> (node_modules/chai-fs/lib/assertions/directory.js:21:53)
      at Function.ctx.<computed> [as directory] (node_modules/chai/lib/chai/utils/addMethod.js:41:25)
      at Function.assert.isDirectory (node_modules/chai-fs/lib/assertions/directory.js:34:35)
      at Context.<anonymous> (test/index-test.js:33:17)
      at processImmediate (node:internal/timers:464:21)



npm ERR! code 6
npm ERR! path /Users/anikabernstein/git-basics-lab-phase-0
npm ERR! command failed
npm ERR! command sh -c mocha --timeout 5000 -R mocha-multi --reporter-options spec=-,json=.results.json

npm ERR! A complete log of this run can be found in:
npm ERR!     /Users/anikabernstein/.npm/_logs/2021-02-27T02_59_39_737Z-debug.log
anikabernstein@anikas-imac git-basics-lab-phase-0 % ls
CONTRIBUTING.md		README.md		package-lock.json	test
LICENSE.md		node_modules		package.json
anikabernstein@anikas-imac git-basics-lab-phase-0 % git status
On branch master
Your branch is up to date with 'origin/master'.

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
	modified:   package-lock.json

no changes added to commit (use "git add" and/or "git commit -a")
anikabernstein@anikas-imac git-basics-lab-phase-0 % pwd
/Users/anikabernstein/git-basics-lab-phase-0
anikabernstein@anikas-imac git-basics-lab-phase-0 % mkdir my-repository
anikabernstein@anikas-imac git-basics-lab-phase-0 % ls
CONTRIBUTING.md		README.md		node_modules		package.json
LICENSE.md		my-repository		package-lock.json	test
anikabernstein@anikas-imac git-basics-lab-phase-0 % open [README.md]  
zsh: no matches found: [README.md]
anikabernstein@anikas-imac git-basics-lab-phase-0 % open README.md 
anikabernstein@anikas-imac git-basics-lab-phase-0 % cd my-repository/ 
anikabernstein@anikas-imac my-repository % ls
anikabernstein@anikas-imac my-repository % git init
Initialized empty Git repository in /Users/anikabernstein/git-basics-lab-phase-0/my-repository/.git/
anikabernstein@anikas-imac my-repository % ls
anikabernstein@anikas-imac my-repository % pwd
/Users/anikabernstein/git-basics-lab-phase-0/my-repository
anikabernstein@anikas-imac my-repository % git status
On branch master

No commits yet

nothing to commit (create/copy files and use "git add" to track)
anikabernstein@anikas-imac my-repository % cd ..
anikabernstein@anikas-imac git-basics-lab-phase-0 % ls
CONTRIBUTING.md		README.md		node_modules		package.json
LICENSE.md		my-repository		package-lock.json	test
anikabernstein@anikas-imac git-basics-lab-phase-0 % npm test

> git-basics-lab@1.0.0 test
> mocha --timeout 5000 -R mocha-multi --reporter-options spec=-,json=.results.json



  this lab
    ✓ has a folder named my-repository
    ✓ has a valid git repository initialized for the my-repository folder
    1) has a README.md file in the my-repository folder

  the local repository
    2) has README.md as a tracked file
    3) has at least one commit
    4) has been pushed up to the remote repository


  2 passing (7ms)
  4 failing

  1) this lab
       has a README.md file in the my-repository folder:
     AssertionError: no README.md file found within "/my-repository": expected './my-repository/README.md' to exist
      at Function.assert.pathExists (node_modules/chai-fs/lib/assertions/path.js:31:35)
      at Context.<anonymous> (test/index-test.js:17:17)
      at processImmediate (node:internal/timers:464:21)

  2) the local repository
       has README.md as a tracked file:
     AssertionError: no files are being tracked.  Use "git add ." to track all files in this repo: expected './my-repository/.git/index' to exist
      at Function.assert.pathExists (node_modules/chai-fs/lib/assertions/path.js:31:35)
      at Context.<anonymous> (test/index-test.js:25:17)
      at processImmediate (node:internal/timers:464:21)

  3) the local repository
       has at least one commit:
     AssertionError: no commits were found.  Use "git commit -m" followed by a message to create a commit: value: expected './my-repository/.git/logs' to exist
      at Function.<anonymous> (node_modules/chai-fs/lib/assertions/directory.js:21:53)
      at Function.ctx.<computed> [as directory] (node_modules/chai/lib/chai/utils/addMethod.js:41:25)
      at Function.assert.isDirectory (node_modules/chai-fs/lib/assertions/directory.js:34:35)
      at Context.<anonymous> (test/index-test.js:29:17)
      at processImmediate (node:internal/timers:464:21)

  4) the local repository
       has been pushed up to the remote repository:
     AssertionError: no record of pushing to a remote was found. Follow the instructions on GitHub to connect and push to a new remote repository: value: expected './my-repository/.git/logs/refs/remotes' to exist
      at Function.<anonymous> (node_modules/chai-fs/lib/assertions/directory.js:21:53)
      at Function.ctx.<computed> [as directory] (node_modules/chai/lib/chai/utils/addMethod.js:41:25)
      at Function.assert.isDirectory (node_modules/chai-fs/lib/assertions/directory.js:34:35)
      at Context.<anonymous> (test/index-test.js:33:17)
      at processImmediate (node:internal/timers:464:21)



npm ERR! code 4
npm ERR! path /Users/anikabernstein/git-basics-lab-phase-0
npm ERR! command failed
npm ERR! command sh -c mocha --timeout 5000 -R mocha-multi --reporter-options spec=-,json=.results.json

npm ERR! A complete log of this run can be found in:
npm ERR!     /Users/anikabernstein/.npm/_logs/2021-02-27T03_30_25_260Z-debug.log
anikabernstein@anikas-imac git-basics-lab-phase-0 % cd my-repository 
anikabernstein@anikas-imac my-repository % touch README.md
anikabernstein@anikas-imac my-repository % ls
README.md
anikabernstein@anikas-imac my-repository % git status
On branch master

No commits yet

Untracked files:
  (use "git add <file>..." to include in what will be committed)
	README.md

nothing added to commit but untracked files present (use "git add" to track)
anikabernstein@anikas-imac my-repository % git add .
anikabernstein@anikas-imac my-repository % npm test

> git-basics-lab@1.0.0 test
> mocha --timeout 5000 -R mocha-multi --reporter-options spec=-,json=.results.json



  this lab
    ✓ has a folder named my-repository
    ✓ has a valid git repository initialized for the my-repository folder
    ✓ has a README.md file in the my-repository folder

  the local repository
    ✓ has README.md as a tracked file
    1) has at least one commit
    2) has been pushed up to the remote repository


  4 passing (7ms)
  2 failing

  1) the local repository
       has at least one commit:
     AssertionError: no commits were found.  Use "git commit -m" followed by a message to create a commit: value: expected './my-repository/.git/logs' to exist
      at Function.<anonymous> (node_modules/chai-fs/lib/assertions/directory.js:21:53)
      at Function.ctx.<computed> [as directory] (node_modules/chai/lib/chai/utils/addMethod.js:41:25)
      at Function.assert.isDirectory (node_modules/chai-fs/lib/assertions/directory.js:34:35)
      at Context.<anonymous> (test/index-test.js:29:17)
      at processImmediate (node:internal/timers:464:21)

  2) the local repository
       has been pushed up to the remote repository:
     AssertionError: no record of pushing to a remote was found. Follow the instructions on GitHub to connect and push to a new remote repository: value: expected './my-repository/.git/logs/refs/remotes' to exist
      at Function.<anonymous> (node_modules/chai-fs/lib/assertions/directory.js:21:53)
      at Function.ctx.<computed> [as directory] (node_modules/chai/lib/chai/utils/addMethod.js:41:25)
      at Function.assert.isDirectory (node_modules/chai-fs/lib/assertions/directory.js:34:35)
      at Context.<anonymous> (test/index-test.js:33:17)
      at processImmediate (node:internal/timers:464:21)



npm ERR! code 2
npm ERR! path /Users/anikabernstein/git-basics-lab-phase-0
npm ERR! command failed
npm ERR! command sh -c mocha --timeout 5000 -R mocha-multi --reporter-options spec=-,json=.results.json

npm ERR! A complete log of this run can be found in:
npm ERR!     /Users/anikabernstein/.npm/_logs/2021-02-27T03_32_29_606Z-debug.log
anikabernstein@anikas-imac my-repository % git commit -m 'First submission'
[master (root-commit) 744c447] First submission
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 README.md
anikabernstein@anikas-imac my-repository % npm test

> git-basics-lab@1.0.0 test
> mocha --timeout 5000 -R mocha-multi --reporter-options spec=-,json=.results.json



  this lab
    ✓ has a folder named my-repository
    ✓ has a valid git repository initialized for the my-repository folder
    ✓ has a README.md file in the my-repository folder

  the local repository
    ✓ has README.md as a tracked file
    ✓ has at least one commit
    1) has been pushed up to the remote repository


  5 passing (8ms)
  1 failing

  1) the local repository
       has been pushed up to the remote repository:
     AssertionError: no record of pushing to a remote was found. Follow the instructions on GitHub to connect and push to a new remote repository: value: expected './my-repository/.git/logs/refs/remotes' to exist
      at Function.<anonymous> (node_modules/chai-fs/lib/assertions/directory.js:21:53)
      at Function.ctx.<computed> [as directory] (node_modules/chai/lib/chai/utils/addMethod.js:41:25)
      at Function.assert.isDirectory (node_modules/chai-fs/lib/assertions/directory.js:34:35)
      at Context.<anonymous> (test/index-test.js:33:17)
      at processImmediate (node:internal/timers:464:21)



npm ERR! code 1
npm ERR! path /Users/anikabernstein/git-basics-lab-phase-0
npm ERR! command failed
npm ERR! command sh -c mocha --timeout 5000 -R mocha-multi --reporter-options spec=-,json=.results.json

npm ERR! A complete log of this run can be found in:
npm ERR!     /Users/anikabernstein/.npm/_logs/2021-02-27T03_33_53_205Z-debug.log
anikabernstein@anikas-imac my-repository % git push
fatal: No configured push destination.
Either specify the URL from the command-line or configure a remote repository using

    git remote add <name> <url>

and then push using the remote name

    git push <name>

anikabernstein@anikas-imac my-repository % npm test

> git-basics-lab@1.0.0 test
> mocha --timeout 5000 -R mocha-multi --reporter-options spec=-,json=.results.json



  this lab
    ✓ has a folder named my-repository
    ✓ has a valid git repository initialized for the my-repository folder
    ✓ has a README.md file in the my-repository folder

  the local repository
    ✓ has README.md as a tracked file
    ✓ has at least one commit
    1) has been pushed up to the remote repository


  5 passing (6ms)
  1 failing

  1) the local repository
       has been pushed up to the remote repository:
     AssertionError: no record of pushing to a remote was found. Follow the instructions on GitHub to connect and push to a new remote repository: value: expected './my-repository/.git/logs/refs/remotes' to exist
      at Function.<anonymous> (node_modules/chai-fs/lib/assertions/directory.js:21:53)
      at Function.ctx.<computed> [as directory] (node_modules/chai/lib/chai/utils/addMethod.js:41:25)
      at Function.assert.isDirectory (node_modules/chai-fs/lib/assertions/directory.js:34:35)
      at Context.<anonymous> (test/index-test.js:33:17)
      at processImmediate (node:internal/timers:464:21)



npm ERR! code 1
npm ERR! path /Users/anikabernstein/git-basics-lab-phase-0
npm ERR! command failed
npm ERR! command sh -c mocha --timeout 5000 -R mocha-multi --reporter-options spec=-,json=.results.json

npm ERR! A complete log of this run can be found in:
npm ERR!     /Users/anikabernstein/.npm/_logs/2021-02-27T03_34_12_751Z-debug.log
anikabernstein@anikas-imac my-repository % git remote add origin git@github.com:anikajb92/git-basics-lab-phase-0.git
anikabernstein@anikas-imac my-repository % git push -u origin main
error: src refspec main does not match any
error: failed to push some refs to 'git@github.com:anikajb92/git-basics-lab-phase-0.git'
anikabernstein@anikas-imac my-repository % git branch -M main                                                       
anikabernstein@anikas-imac my-repository % git push -u origin main
Warning: Permanently added the RSA host key for IP address '140.82.113.3' to the list of known hosts.
Enumerating objects: 3, done.
Counting objects: 100% (3/3), done.
Writing objects: 100% (3/3), 219 bytes | 219.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0)
remote: 
remote: Create a pull request for 'main' on GitHub by visiting:
remote:      https://github.com/anikajb92/git-basics-lab-phase-0/pull/new/main
remote: 
To github.com:anikajb92/git-basics-lab-phase-0.git
 * [new branch]      main -> main
Branch 'main' set up to track remote branch 'main' from 'origin'.
anikabernstein@anikas-imac my-repository % npm test

> git-basics-lab@1.0.0 test
> mocha --timeout 5000 -R mocha-multi --reporter-options spec=-,json=.results.json



  this lab
    ✓ has a folder named my-repository
    ✓ has a valid git repository initialized for the my-repository folder
    ✓ has a README.md file in the my-repository folder

  the local repository
    ✓ has README.md as a tracked file
    ✓ has at least one commit
    ✓ has been pushed up to the remote repository


  6 passing (5ms)

anikabernstein@anikas-imac my-repository % cd ..
anikabernstein@anikas-imac git-basics-lab-phase-0 % npm test

> git-basics-lab@1.0.0 test
> mocha --timeout 5000 -R mocha-multi --reporter-options spec=-,json=.results.json



  this lab
    ✓ has a folder named my-repository
    ✓ has a valid git repository initialized for the my-repository folder
    ✓ has a README.md file in the my-repository folder

  the local repository
    ✓ has README.md as a tracked file
    ✓ has at least one commit
    ✓ has been pushed up to the remote repository


  6 passing (6ms)

anikabernstein@anikas-imac git-basics-lab-phase-0 % git add .
warning: adding embedded git repository: my-repository
hint: You've added another git repository inside your current repository.
hint: Clones of the outer repository will not contain the contents of
hint: the embedded repository and will not know how to obtain it.
hint: If you meant to add a submodule, use:
hint: 
hint: 	git submodule add <url> my-repository
hint: 
hint: If you added this path by mistake, you can remove it from the
hint: index with:
hint: 
hint: 	git rm --cached my-repository
hint: 
hint: See "git help submodule" for more information.
anikabernstein@anikas-imac git-basics-lab-phase-0 % cd /my-repository
cd: no such file or directory: /my-repository
anikabernstein@anikas-imac git-basics-lab-phase-0 % cd my-repository 
anikabernstein@anikas-imac my-repository % git add .
anikabernstein@anikas-imac my-repository % git commit -m 'Done with assignment'
On branch main
Your branch is up to date with 'origin/main'.

nothing to commit, working tree clean
anikabernstein@anikas-imac my-repository % open .
anikabernstein@anikas-imac my-repository % cd ..
anikabernstein@anikas-imac git-basics-lab-phase-0 % pwd
/Users/anikabernstein/git-basics-lab-phase-0
anikabernstein@anikas-imac git-basics-lab-phase-0 % git push origin master
Warning: Permanently added the RSA host key for IP address '140.82.112.3' to the list of known hosts.
Everything up-to-date
anikabernstein@anikas-imac git-basics-lab-phase-0 % git add README.md
anikabernstein@anikas-imac git-basics-lab-phase-0 % git remote -v
origin	git@github.com:anikajb92/git-basics-lab-phase-0.git (fetch)
origin	git@github.com:anikajb92/git-basics-lab-phase-0.git (push)
anikabernstein@anikas-imac git-basics-lab-phase-0 % 
