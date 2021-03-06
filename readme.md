h1. What is it?
This is bunch of Eclipse Virgo plans to enable a fully-fledged osgiliath ESB project

h2. How to use?

First you have to configure your maven settings.xml to mirror the osgiliath nexus (http://nexus.osgiliath.net/nexus/content/groups/public/) or install superpom and helpers projects.
If you mirror it, please be cool with my 6 years old machine and proxy with your proper Nexus (or even better, clone and push it to m2).

In a second time, configure in this file a maven active profile with the property virgo.path pointing on your root Virgo-jetty installation (3.6.0.RELEASE at the time I'm writing). 
Add entry javax.persistence.metamodel to the spring orm MANIFEST (on the repository/ext folder).

Finally just run mvn clean install and launch Virgo!

h2. Architecture

You can clone the git project at https://github.com/Tcharl/virgo.plans.git

It's composed of a parent pom and multiples modules (plans):

* derby for the database
* jpa for persistence
* validation for hibernate validation (with an osgi service)
* security for spring security
* messaging with camel for jms and websocket (jms connection is exported)
