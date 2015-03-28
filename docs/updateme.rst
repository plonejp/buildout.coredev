.. -*- coding: utf-8 -*-

========================
How to Update these Docs
========================

These documents are currently stored with the coredev buildout in github in :file:`/docs`.
To update them,
please checkout the coredev buildout and update there.
Make the changes on the latest version branch (as of this writing ``5.0``)::

  > git clone git@github.com:plone/buildout.coredev.git
  > cd buildout.coredev
  > git checkout 5.0

To test your changes locally,
re-run buildout and then::

  > bin/sphinx-build docs docs/build

Sphinx will poop out a directory that you can put in your browser to validate.
For example: ``file:///home/user/buildout.coredev/docs/build/index.html``

Please make sure to validate all warnings and errors before committing to make sure the documents remain valid.
Once everything is ready to go,
commit and push changes.

Cherry pick commits on the latest branch to the currently released branch
(as of this writing ``4.3``)
if these changes apply to that version
(you can get the SHA hash from :command:`git log`)::

  > git checkout 4.3
  > git cherry-pick b6ff4309

There may be conflicts;
if so,
resolve them and then follow the directions git gives you to complete the :command:`git cherry-pick`.
