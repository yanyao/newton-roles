=========================
OpenStack-Ansible Horizon
=========================

.. toctree::
   :maxdepth: 2

   configure-horizon.rst

This Ansible role installs and configures OpenStack Horizon served by the
Apache webserver. Horizon is configured to use Galera for session caching and
Memcached for other caching.

Default variables
~~~~~~~~~~~~~~~~~

.. literalinclude:: ../../defaults/main.yml
   :language: yaml
   :start-after: under the License.


Required variables
~~~~~~~~~~~~~~~~~~

This list is not exhaustive. See role internals for further
details.

.. code-block:: yaml

      horizon_galera_address: 10.100.100.101
      horizon_container_mysql_password: "SuperSecrete"
      horizon_secret_key: "SuperSecreteHorizonKey"


Example playbook
~~~~~~~~~~~~~~~~

.. literalinclude:: ../../examples/playbook.yml
   :language: yaml

Tags
====

This role supports two tags: ``horizon-install`` and ``horizon-config``.

The ``horizon-install`` tag can be used to install and upgrade.

The ``horizon-config`` tag can be used to manage configuration.
