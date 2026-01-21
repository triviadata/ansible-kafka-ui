Kafka UI
=========

[![Build Status](https://travis-ci.com/triviadata/ansible-kafka-ui.svg?branch=master)](https://travis-ci.com/triviadata/ansible-kafka-ui)

Install Kafka UI on Linux host.

Requirements
--------------
Java must be installed on the target host.

Role Variables
--------------
Variables are listed in `defaults/main.yml` and described below:

* **kafka_ui_version**: Version of Kafka UI to install
* **kafka_ui_user**: System user for Kafka UI service
* **kafka_ui_group**: System group for Kafka UI service
* **kafka_ui_install_dir**: Installation directory
* **kafka_ui_config_dir**: Configuration directory
* **kafka_ui_port**: Port for Kafka UI web interface
* **kafka_ui_java_opts**: Java options for the application
* **kafka_ui_download_url**: URL to download Kafka UI jar
* **kafka_ui_clusters**: List of Kafka clusters to monitor

Dependencies
----------------
None.

Example Playbook
----------------

    - hosts: servers
      roles:
         - role: triviadata.kafka-ui
           kafka_ui_clusters:
             - name: production
               bootstrap_servers: kafka1:9092,kafka2:9092
               zookeeper: zk1:2181,zk2:2181

License
-------

BSD

Author Information
-------
This role was created in January 2026 by Matus Cuper
