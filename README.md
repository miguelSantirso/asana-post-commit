Fork by Miguel Santirso
=======================

This is a very simple fork just to slightly alter the messages posted to asana as comments.

Instead of just including a short hash of the commit, we include the full URL to the commit in Bitbucket.


README
======

A git post-commit script to comment on / close Asana tickets. Read the blog post with more detail here: [http://www.ultrajoke.net/2013/01/integrating-asana-and-git/](http://www.ultrajoke.net/2013/01/integrating-asana-and-git/)

tl;dr:

Copy the post-commit file to your repo's root `.git/hooks` directory. It's probably not a great idea to actually clone the repo into the internals of your repo. I don't know that it will break anything, but I don't guarantee it won't.

Then run the following command:

`% git config --global user.asana-key "MY_ASANA_API_KEY" # (get the api key at http://app.asana.com/-/account_api)`

Then chmod your hooks folder:
`% chmod 655 .git/hooks`

Now in your commits, you can write messages like "Tweaked the widget; fixed #1, #2, and #3; references #4 and #5; oh yeah, and closes #6" and the right thing will happen.

