Welcome to the testwikidocs_sync wiki!

This is a test page.

Trying out another change....

Test

Now trying an update from the umbrella repo

Now trying a fork and PR

------------

Ok it works so workflow with a `metarepo/docs` copied from `metarepo/<submodule>` folder seems to be:

If there are Edits on the Wiki then in `metarepo/<submodule>`:

1. `git submodule update --remote --merge` from `metarepo`

2. cp .md files in `metarepo/<submodule>` to `metarepo/docs` to update live docs website


If there are PRs to files in `metarepo/docs` then either manually merge on Wiki OR:

0. `git pull origin master` from `metarepo`

1. Do `git submodule update --remote --merge` from `metarepo`

2. if there were Wiki udpates cp .md files from `metarepo/<submodule>` to `metarepo/docs`

3. human: manually review PR to `metarepo/docs` if accepted then:

4. copy any changes from `metarepo/docs` to  `metarepo/<submodule>` 

5. Just in case do a `git submodule update --remote --rebase` from `metarepo`

6. Fix any conflicts

7. git commit updates

8. `git push origin master` from `metarepo/<submodule>`

9. (human: verify Wiki is udpated)

Does this work?
