=======
Midonet
=======

MidoNet is an advanced Software Defined Networking (SDN) solution, which provides network virtualization for public and private cloud environments.

Sample pillars
==============

Cluster Control
----------------

.. code-block:: yaml

    midonet:
      control:
        version: v5.0
        enterprise:
          enabled: true
        enabled: true
        host: 127.0.0.1
        nova:
          control:
            host: 127.0.0.1
        database:
          members:
          - host: 127.0.0.1
            port: 9160
          - host: 127.0.0.1
            port: 9160
          - host: 127.0.0.1
            port: 9160
        zookeeper:
          members:
          - host: 127.0.0.1
          - host: 127.0.0.1
          - host: 127.0.0.1
        identity:
          user: midonet
          password: passwd
          host: 127.0.0.1
          admin:
            token: tokenpass
            password: passwd

Analytics
-----------

.. code-block:: yaml

    midonet:
      analytics:
        version: v5.0
        enterprise:
          enabled: true
        enabled: true
        host: 127.0.0.1

Gateway
--------

.. code-block:: yaml

	midonet:
      gateway:
	    version: v5.0
	    enterprise:
	      enabled: true
	    enabled: true
	    zookeeper:
	      members:
	      - host: 127.0.0.1
	      - host: 127.0.0.1
	      - host: 127.0.0.1
	    template: medium

Compute
--------

.. code-block:: yaml

	midonet:
      compute:
	    version: v5.0
	    enterprise:
	      enabled: true
	    enabled: true
	    zookeeper:
	      members:
	      - host: 127.0.0.1
	      - host: 127.0.0.1
	      - host: 127.0.0.1
	    template: medium

Web
----

.. code-block:: yaml

	midonet:
	  web:
	    version: v5.0
	    enabled: true
	    api:
	      host: 127.0.0.1
	    analytics:
	      host: 127.0.0.1

Read More
=========

* http://www.midokura.com/midonet/
Documentation and Bugs
======================

To learn how to install and update salt-formulas, consult the documentation
available online at:

    http://salt-formulas.readthedocs.io/

In the unfortunate event that bugs are discovered, they should be reported to
the appropriate issue tracker. Use Github issue tracker for specific salt
formula:

    https://github.com/salt-formulas/salt-formula-midonet/issues

For feature requests, bug reports or blueprints affecting entire ecosystem,
use Launchpad salt-formulas project:

    https://launchpad.net/salt-formulas

You can also join salt-formulas-users team and subscribe to mailing list:

    https://launchpad.net/~salt-formulas-users

Developers wishing to work on the salt-formulas projects should always base
their work on master branch and submit pull request against specific formula.

    https://github.com/salt-formulas/salt-formula-midonet

Any questions or feedback is always welcome so feel free to join our IRC
channel:

    #salt-formulas @ irc.freenode.net
