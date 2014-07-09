Liferay Spring Portlet MVC
==========================

A Liferay Spring Portlet MVC project template using Maven.

* Liferay EE 6.2.10.4 (GA1, SP3)
* Java 1.7
* Portlet 2.0
* Spring Framework 4.0.6
* Annotation-based controller configuration

Usage
-----
```bash
$ git clone http://github.com/psvehla/liferay-spring-mvc-portlet.git
$ cd liferay-spring-mvc-portlet
$ mvn package
```

Deploy
------
If you're using Liferay Portal with Tomcat, copy the war to the deploy directory.

```
$ cp target/liferay-spring-mvc-portlet.war $LIFERAY_HOME/deploy/
```

Configuration
-------------

Default settings are Liferay EE 6.2.10.4, Java 1.7, Portlet 2.0, and Spring 4.0.  All can be configured in [pom.xml](https://github.com/psvehla/liferay-spring-mvc-portlet/pom.xml)

```xml
	<properties>
		<liferay.version>6.2.10.4</liferay.version>
		<liferay.auto.deploy.dir>F:\java\liferay-portal-6.1.20-ee-ga2\deploy</liferay.auto.deploy.dir>
		<java-version>1.7</java-version>
		<portlet-api.version>2.0</portlet-api.version>
		<servlet-api.version>2.5</servlet-api.version>
		<jsp-api.version>2.2</jsp-api.version>
		<jstl.version>1.2</jstl.version>
		<org.springframework-version>4.0.6.RELEASE</org.springframework-version>
		<org.aspectj-version>1.8.1</org.aspectj-version>
		<org.slf4j-version>1.7.7</org.slf4j-version>
	</properties>
```

Archetype
---------

The main point of this project is to create a Maven archetype.

Add an entry for the archetype in: ```~/.m2/archetype-catalog.xml```

```xml
<archetype>
  <groupId>au.com.redbarn</groupId>
  <artifactId>liferay-spring-mvc-portlet-archetype</artifactId>
  <version>1.3-RELEASE</version>
  <repository>https://raw.github.com/psvehla/maven-repo/master/releases</repository>
  <description>liferay-spring-mvc-portlet-archetype</description>
</archetype>
```

Run the maven archetype generate command.  Follow the prompts to specify the groupId, artifactId, and version for your project.

```bash
$ mvn archetype:generate -DarchetypeCatalog=local
```

Licence
-------

Copyright 2014 Red Barn Consulting

Licenced under the LGPL Licence, Version 3.0: http://www.gnu.org/licenses/lgpl.html
