# Documentation :: izpack by org.apache.easyant.plugins

# Description

This module provides izpack integration feature.
	
# Example

```xml
<ea:plugin organisation="org.apache.easyant.plugins" module="izpack" revision="0.1"/>
```
Organisation attribute is optional. If not specified default one will be used.

```xml
<ea:plugin module="izpack" revision="0.1"/>
```

## Available targets

|target name|description|extension point|depends|
|-----------|-----------|---------------|-------|
|izpack:init||||
|izpack:install|||izpack:init|

## Module parameters

### Properties

|property|description|required|default value|
|--------|-----------|--------|-------------|
|izpack.input|the XML installation file. The installation can be specified as an external file, or embedded using a config child element.|false|/home/neoverflow/projects/easyant/community-plugins/izpack-easyant-plugin/src/main/izpack/install.xml|
|izpack.basedir|the base directory to resolve the relative paths|false|/home/neoverflow/projects/easyant/community-plugins/izpack-easyant-plugin/src/main/izpack|
|target.artifacts|destination directory for target artifacts|false|${target}/artifacts|
|izpack.installer.type|optional. standard or web. If web, the 'webdir' attribute must be specified in the input file. Used to force creation of a standard installer when the 'webdir' attribute has been used.|false|standard|
|izpack.homedir|the IzPack home directory|false|/home/neoverflow/.izpack|
|izpack.output|the output jar installer file|false|${target.artifacts}/${ivy.module}-install.jar|

## Ivy Configurations

|name|description|extends|visibility|deprecated|
|----|-----------|-------|----------|----------|
|default|runtime dependencies artifact can be used with this conf|[]|public||
|test|this scope indicates that the dependency is not required for normal use of the application, and is only available for the test compilation and execution phases.|[]|private||
|provided|this is much like compile, but indicates you expect the JDK or a container to provide it. It is only available on the compilation classpath, and is not transitive.|[]|public||

## Dependencies Overview

|Organisation|Module|Revision|
|org.codehaus.izpack|izpack-ant|5.0.0-beta11|
|org.codehaus.izpack|izpack-compiler|5.0.0-beta11|
|org.codehaus.izpack|izpack-uninstaller|5.0.0-beta11|
|org.codehaus.izpack|izpack-installer|5.0.0-beta11|

