Title: Translations
Status: hidden

Here's a short guide about creating or modifying translations for Yorg.

This guide assumes several prerequisites. This would be the optimal path for creating the translations since you would be credited as a contributor on GitHub. Anyway, if you don't want to follow it, feel free to:

* edit the file [your_language.po](https://github.com/cflavio/yorg/tree/testing/assets/po) for your language and [send it to me]({filename}/pages/about.md) (if your language already exists) or send it to the mailing list (see later);
* edit the [template file](https://github.com/cflavio/yorg/blob/testing/assets/po/yorg.pot) and [send it to me]({filename}/pages/about.md) or send it to the mailing list (see later) if your language doesn't exist.

Please note that the following guide doesn't pollute your system: you can safely remove everything with `rm -rf yorg` when you want.

* if your language hasn't been added already, please [contact me]({filename}/pages/about.md) so i can implement the needed modifications (and wait for them)
* clone the repository: `git clone --recursive https://github.com/cflavio/yorg.git`
* go into the directory: `cd yorg`
* checkout the branch you want to work on (one of *master*, *testing*, *stable*): `git checkout <branchname>; git submodule foreach git checkout <branchname>`
* create a python2 virtualenv: `virtualenv --python=/usr/bin/python2 venv`
* activate the virtualenv: `. ./venv/bin/activate`
* install the prerequisites: `pip install panda3d SCons`
* build the required assets: `scons lang=1 images=1 tracks=1`
* edit the file `assets/po/<your_language>.po`
* rebuild the language files `scons lang=1`
* launch the game so you can test your translation: `python main.py`
* create a pull request for [Yorg](https://github.com/cflavio/yorg) which contains your `assets/po/<your_language>.po` file, so I can pull your modifications (and you will be added as a contributor of the project on GitHub automatically)

Very important!
===============

Please, send an empty email to <mailto:ya2_l10n-join@ya2.it> in order to subscribe l10n's mailing list. So, you can receive messages from us when the development of a new version is completed and new translations are needed. You can easily unsubscribe when you want. Please **note**: we reject requests of subscription from unknown people, so make sure that you've informed us about your contribution [somewhere]({filename}/pages/community.md). Thank you!

Please note that we will send few emails (once a release), so you won't be swamped by our emails. Moreover, you can keep in contact with other translators and developers with this mailing list.

We need it in order to keep in contact with the translators (otherwise, reaching them singularly would require a lot of time). Thank you very much!
