## Description
A wrapper around [Datomic Free](http://downloads.datomic.com/free.html) that makes it easy to
start Datomic Free transactors and upgrade to newer versions.

## Usage

For first time users:

```sh
$ git clone https://github.com/cldwalker/datomic-free.git ~/.datomic-free
$ ~/.datomic-free/bin/datomic-free start

# To make it easy to use `datomic-free` add an alias to your bashrc/zshrc
$ echo 'alias datomic-free=$HOME/.datomic-free/bin/datomic-free' >> ~/.zshrc
$ . ~/.zshrc
$ datomic-free start

# To specify transactor.properties (Absolute path only)
$ datomic-free start /absolute/path/to/transactor.properties

# To migrate existing data/ to datomic-free
$ rm -rf ~/.datomic-free/data
$ cp -R $OLD_DATOMIC_REPO/data  ~/.datomic-free/
```

Whenever you'd like to update to the latest Datomic Free:

```sh
$ datomic-free update
```

This new version is now the active datomic-free version. Since datomic-free keeps data outside
of versions in ~/.datomic-free/data, you use the same data across versions *by default*.

To update to a specific version, pass a version:

```sh
$ datomic-free update 0.8.3627
```

To use another version you've already installed:

```sh
$ datomic-free use 0.8.3646
```

## License
See LICENSE.txt. This project is in no way affiliated with Datomic (Metadata Partners, LLC).

## Credits
* Thanks to @richhickey and @stuarthalloway for datomic
* Thanks to @rkneufeld for the downloading function of the shell script
* Bug fixes: @sherbondy

## TODO
* Allow other config and args to bin/transactor
* rest command to execute bin/rest
* better help
* better exit codes
* better error checking for use
* convert this readme to a man page
