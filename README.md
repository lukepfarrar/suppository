
Super Simple Apt Repository (suppository)
=========================================

Update:
-------

After 3 years of faithful service this has been [replaced](https://github.com/TheBookPeople/suppository) by [wgriffiths](https://github.com/wgriffiths).
The new ruby version is space efficient and much faster, but still does not require any DB etc. (These scripts recreate all the Package files etc.
which requires checksumming of all packages).

Introduction
------------

These bash scripts create & maintain a simple apt repository.

Reprepro would have been perfect for my needs, if only it supported multiple versions
of a package. Everything else seems very heavyweight, I just wanted something I could call from Jenkins that generate files to be served by apache.

This is desirable for internal repositories which may want to be able to roll back etc.

GPG Signing
-----------

The scripts assume that you are signing the repository
A GPG key needs to be generated for your user first with

 gpg --gen-key

Usage
-----

* suppository-create - creates a new repository
* suppository-add - adds a .deb file to the repository
* suppository-generate - regenerates Packages and Releases files. Run this if you have manually changed the repository, i.e. removed package files etc.



