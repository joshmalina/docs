A common development workflow looks like this

1. Make your edits on your local copy of your project
2. Push those edits to a online repository somewhere, i.e. Github.com
3. Pull the changes down from Github to your live server when you're ready to *go live* i.e. *deploy* your changes.

This is all great, assuming your live server host has Git installed, or at the very least allows you SSH access and the ability to install it yourself. With many shared servers, though, this isn't always the case. 

Fortunately, if this applies to you, you can still get most of the benefits of Version Control / Git, you can just circumvent the last step by using rsync to transfer your files instead of git.

Your workflow would then look like this:

1. Make your edits on your local copy of your project
2. Push those edits to an online repository somewhere, i.e. Github.com
3. Rsync your changes from your local server to your live server

In order to accomplish Step #3, we'll use the rsync command:

	rsync source/ destination/
	
Lets adapt that for our purposes:

	rsync -rtvu /Users/username/Sites/sitename/ username@server.com:/home/username/www/sitename/
	
Lets break down the flags we're using:

r = Recursively sync through all the folder
t = Preserve file modification times
v = Verbose...i.e. have rsync tell us what it's doing as it's doing
u = Only mirror changed files (rather than copying everything everytime)

After the flags, we see the path to your local project you want to copy, followed by the path to the destination on the live server. The latter is prefixed with your server login.

References:
[Synchornizing folders with rsync](http://www.jveweb.net/en/archives/2010/11/synchronizing-folders-with-rsync.html)

