## Description
A wrapper around [datomic-free](http://downloads.datomic.com/free.html) that makes it easy to
start and upgrade datomic-free transactors and other datomic executables.

## Usage

For first time users:

```sh
$ git clone https://github.com/cldwalker/datomic-free.git
$ cd datomic-free
$ bin/datomic-free start
```

Whenever you'd like to update to the latest datomic-free:

```sh
$ bin/datomic-free update
```

To update to a specific version, pass a version:

```sh
$ bin/datomic-free update 0.8.3627
```

To use another version you've already installed:

```sh
$ bin/datomic-free use 0.8.3646
```

## License
See LICENSE.txt. This project is in no way affiliated with Datomic (Metadata Partners, LLC).

## Credits
* Thanks to @richhickey and @stuarthalloway for datomic
* Thanks to @rkneufeld for the downloading function of the shell script

## TODO
* Move/use existing data/config dirs
* Allow other config and args to bin/transactor
* rest command to execute bin/rest
* better help
* better exit codes
* better error checking for use
* convert this readme to a man page
