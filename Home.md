:) Welcome to the testwikidocs_sync wiki!

This is a test page.

Trying out another change....

Test

Now trying an update from the umbrella repo

Now trying a fork and PR

------------

Ok it works so workflow with a `metarepo/docs` copied from `metarepo/<submodule>` folder seems to be:

Edits on Wiki only then in `metarepo/<submodule>`:

1. git pull
2. cp to `metarepo/docs`

PRs in `metarepo/docs` then either manually merge on Wiki or:

1. accept PR to `metarepo/docs`

2. update `metarepo/<submodule>` from Wiki and copy changes to a branch

3. `git submodule update --remote --rebase` or merge

4. Fix any conflicts

5. `git push --recurse-submodules=check`
