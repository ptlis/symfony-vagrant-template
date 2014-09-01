# Default Symfony2 & Vagrant Installation

Pre-configured Symfony2 & Vagrant template project.

This template consists of the base Symfony2 packages plus a collection of additional packages that I commonly use. This currently includes:

* [Braincrafted Bootstrap Bundle](http://bootstrap.braincrafted.com/)
* [Doctrine Fixtures Bundle](http://symfony.com/doc/current/bundles/DoctrineFixturesBundle/index.html)
* [Doctrine Migrations Bundle](http://symfony.com/doc/current/bundles/DoctrineMigrationsBundle/index.html)
* [JMS Serializer Bundle](https://github.com/schmittjoh/JMSSerializerBundle)
* [Guzzle](http://guzzlephp.org/)


# Requirements

Software & minimum tested versions:

* Vagrant 1.5.
* Virtualbox 4.3.
* Ansible 1.5.


# Box configuration

To see the full details see the contents of the ```provision/``` directory.

In brief, the following packages are installed:

* MariaDB server & client
* Apache2
* php5 (with mysql, curl, intl extensions)
