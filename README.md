Getting a spine app running out-of-the-box
==========================================

Date: October 08, 2012

[Spine][spine] is a fantastic MVC framework that I started working with. Mainly
because I wanted a clear distinction between Model/View/Controller code and I
wanted to write in [coffee-script][] along with documentation in coffee-script.
I also really liked the ease of creating, building, and developing that [hem][]
and the [Spine.app][spine-app] suite offered.

One of the biggest hill I had to climb was because of the nature of evolving
code. Spine, Hem, and Spine.app the three main components in using spine
out-of-the-box was missing some options to let an app built with the one
`spine app myApp` command. To explain this I created this sample to show the
step I had to take to get things running smoothly. It is assumed that many of
these issues will be resolved in future versions. However as of the writing of
this the latest versions have not been published and the fixes were over 3
months old. What this means is that the code you get from the node repository
is about 3 months out of date and that is the crux of the problem.

#### Declaimer ####

Please understand that this documentation is dated information and will be
obsolete as new versions of spine and hem are released.

[hem]: https://github.com/maccman/hem
[spine]: https://github.com/maccman/spine
[spine-app]: https://github.com/maccman/spine.app
[coffee-script]: http://coffeescript.org/

## Setup ##

The latest versions are available on [github](http://github.com) and you have
to specifically tell npm to install from the git repository and not the npm
registry as they are out of date.

    $ sudo npm install -g git://github.com/maccman/spine.app.git

This will instal the latest edge version of Spine.app and spine. It also
installs version **0.1.9** of hem (which is out of date as well) so we will
upgrade hem:

    $ sudo npm install -g git://github.com/maccman/hem.git

Now you are ready to create your first application:

    $ spine app myApp