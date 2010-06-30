# localenv #

localenv is a script for automatically shelling into and out of the environment configuration required to use a `local::lib` environment. It's rather like virtualenv for Python; in fact, the `activate` script it generates is cribbed mostly from virtualenv for Python.

localenv is designed to work with [cpanminus][] for installing Perl modules.

## Usage ##

    $ localenv myenv
    $ source myenv/bin/activate
    (myenv)$ cpanm Bot::BasicBot::Pluggable  # or whatever
    (myenv)$ perldoc -l Bot::BasicBot::Pluggable
    /home/username/myenv/lib/perl5/Bot/BasicBot/Pluggable.pm
    (myenv)$ deactivate
    $ perldoc -l Bot::BasicBot::Pluggable
    No documentation found for "Bot::BasicBot::Pluggable".

## Requirements ##

* Python 2.4
* [`local::lib`][llib]
* [cpanminus][] (not strictly required but strongly encouraged)

[llib]: http://search.cpan.org/~getty/local-lib-1.006004/lib/local/lib.pm
[cpanminus]: http://search.cpan.org/~miyagawa/App-cpanminus-1.0004/lib/App/cpanminus.pm

## Installation ##

1. Copy the `localenv` script to your `bin` directory and make sure it's executable.
