Slack Rails Continuous Integration
==================================

![Screenshot](slack-rails-ci.png?raw=true "Screenshot")

A Git hook (Bash script) that runs the test suite of a Ruby On Rails application after each commit and posts the result
on a Slack channel - basically, a continuous integration solution cheaper than Travis (but not so good).

Just copy `variables.sh.example` to `variables.sh`, copy the files `post-commit` and `variables.sh` to `.git/hooks` (or symlink them) on the root of your repository and set the variables `$webhook_url` and `$channel` on `variables.sh`.

The script tries to run the test suite with code coverage, but if it's not available, it just runs the tests.

This used to be a Gist at https://gist.github.com/caiosba/d69be6e7e343e27a9e62.
