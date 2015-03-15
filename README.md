# Packer PHP vagrant box builder

## Introduction

Using [packer.io](https://packer.io), build and provision a [Vagrant](https://www.vagrantup.com/) box capable of running a LAMP stack application.

## Usage

A number of builders are included in `build.json` for various versions of PHP, as well as another for HHVM.
To build a PHP 5.6 box, for example, specify that builder name in the `only` argument:

	packer build -only="virtualbox-iso-debian" build.json

You can also build multiple boxes at once, either by specifying specific builder names in the `only`
argument, or just not giving the argument at all:

	packer build -only="virtualbox-iso-debian-php56,virtualbox-iso-debian-hhvm" build.json

	packer build build.json
