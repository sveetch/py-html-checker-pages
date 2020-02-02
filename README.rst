.. _Optimus: https://github.com/sveetch/Optimus
.. _Py Html Checker: https://github.com/sveetch/py-html-checker

=====================
Py Html Checker pages
=====================

A project to prototype and maintain `Py Html Checker`_ exporter templates.

Install
*******

This requires make, Python3, Virtualenv, Pip and C build toolchain to compile
C modules.

::

    make install

Usage
*****

Just build everything : ::

    make build

Then run a basic HTTP server to see it: ::

    make run

This is just a quick way to start. There is much more available commands, see
help for more details: ::

    make help

You should know than commonly to work on your templates and CSS in live, you
will need to launch a watcher for templates, a watcher for Sass sources and a
basic HTTP server, you will find these commands in Makefile help.

Finally when you are done, you can build your pages for production environment
(search for ``-prod`` actions in makefile help).

Overview
********

Optimus
    The static site builder used to build your project. Everything you need to
    know to manage page, project settings, assets and translations is
    on `Optimus documentation <https://optimus.readthedocs.org/>`_
Jinja
    Template syntax engine used in your page templates.
    `Jinja documentation <http://jinja.pocoo.org/docs/>`_.
CSS
    In this project it involves:

    * `Sass <https://sass-lang.com/>`_: the syntax used to write sources to
      build CSS stylesheets;
    * `Boussole <https://boussole.readthedocs.io/>`_: the tool used to build
      CSS from Sass sources;
    * `ITCSS <https://www.xfive.co/blog/itcss-scalable-maintainable-css-architecture/>`_:
      a structured methodology for Sass/CSS sources files used for shipped Sass
      sources;

Development
***********

This project help to maintain page templates and CSS stylesheet for
`Py Html Checker`_ HTML exporter.

It has been built with `Optimus`_ builder, but keep in mind than
`Py Html Checker`_ does not run with Optimus and so won't have all its
available features such as assets management, i18n, custom Jinja extensions,
etc.. You will have to stand on `Py Html Checker`_ exporter limits.

If these limits are respected you should be able to replace `Py Html Checker`_
templates with your own and possibly replace the CSS stylesheet also.
