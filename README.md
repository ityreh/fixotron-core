# fixT
Tools for the Financial Information eXchange protocol

To build this project use

    mvn install

To run the project you can execute the following Maven goal

    mvn camel:run

To deploy the project in OSGi. For example using Apache ServiceMix
or Apache Karaf. You can run the following command from its shell:

    osgi:install -s mvn:de.ityreh.finance/fixt/0.0.1-SNAPSHOT

For more help see the Apache Camel documentation

    http://camel.apache.org/

