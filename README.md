Nutch indexer-elastic2
======================

This is a Nutch plugin for indexing documents using Elasticsearch 2.x.

## Installation

1) Copy this plugin into your nutch plugin directory `$NUTCH_HOME/src/plugin`.

2) Add the required plugin to your `NUTCH_HOME/src/plugin/build.xml`.
```
<!-- NUTCH_HOME/src/plugin/build.xml -->

<project name="Nutch" default="deploy-core" basedir=".">
  ...
  <target name="deploy">
    ... 
    <ant dir="indexer-elastic2" target="deploy"/>
  </target>
  ...
  <target name="clean">
    ...
    <ant dir="indexer-elastic2" target="clean"/>
  </target>
  ...
</project>
```

3) Make sure you have plugin name included in your nutch configuration file `NUTCH_ROOT/conf/nutch-site.xml`
```
<!-- NUTCH_HOME/conf/nutch-site.xml -->

<configuration>
  ...
  <property>
    <name>plugin.includes</name>
    <value>urlfilter-regex|parse-(html|tika)|index-(basic|anchor)|urlnormalizer-(pass|regex|basic)|scoring-opic|indexer-elastic2</value>
  </property>
  ...
</configuration>
```
4) Compile using ant
