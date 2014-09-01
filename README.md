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

* Vagrant 1.5
* Virtualbox 4.3
* Ansible 1.5


# Box configuration

To see the full details see the contents of the ```provision/``` directory.

In brief, the following packages are installed:

* MariaDB server & client
* Apache2
* php5


# Use

* System config changes can be made by editing ```provision/setup/vars/main.yml```.
* Default IP is 169.254.10.10 - this can be changed by editing the Vagrantfile.
* Make sure you configure your hosts file to point the configured hostname to the above (or your custom) IP address.
* Run ```vagrant up```
* Visit your application's host in a web browser.
