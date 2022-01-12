phpenv-man
=========

phpenv-man is a plugin for [phpenv] to easily access the man pages for the
currently set Ruby version, e.g. `ruby(1)` and `irb(1)`.

Technically, phpenv-man is a wrapper for `man(1)` that takes care of using the
correct manpath.

Installation
------------

To install phpenv-man, clone this repository into your `~/.phpenv/plugins`
directory. (You'll need a recent version of phpenv that supports plugin
bundles.)

    $ mkdir -p "$(phpenv root)/plugins"
    $ git clone https://github.com/madumlao/phpenv-man.git "$(phpenv root)/madumlao/phpenv-man"


Usage
-----

Simply use phpenv-man in the same way as your system's `man(1)` program. All
command-line options are passed through to it.

Some examples:

* Show `php(1)` manual:

        $ phpenv man php

* Show `phar(1)` manual:

        $ phpenv man 1 phar

* Print location of `php(1)` manual:

        $ phpenv man -w php
        /home/madumlao/.phpenv/versions/7.4/share/man/man1/php.1

* Change PHP version and print new location of man page:

        $ phpenv global 7.3.25
        $ phpenv man -w php
        /home/mlafeldt/.phpenv/versions/7.3.24/share/man/man1/php.1


License
-------

phpenv-man does not reach the [threshold of originality], so no license is needed.

phpenv-man is based on [rbenv-man].


[phpenv]: https://github.com/phpenv/phpenv
[rbenv-man]: https://github.com/mlafeldt/rbenv-man
[threshold of originality]: http://en.wikipedia.org/wiki/Threshold_of_originality
