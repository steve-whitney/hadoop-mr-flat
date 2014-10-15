# hadoop-mr-flat

Using maven archetypes allows a developer to quickly bootstrap into a new project. IDEs such as IntelliJ are known to support project creation from archetypes.

This is a simple maven archetype based on ch05 of 3rd edition of __Hadoop: The Definitive Guide__ (cref: https://github.com/tomwhite/hadoop-book/tree/3e ).

This project is purposed to be built as an archetype, which can be used to bootstrap other hadoop-mr projects. Please note that I had to "flatten" the maven project structure (hadoop-book uses maven submodules, with which `mvn archetype:create-from-project` apparently doesn't play well).

Although I've installed 1.1-SNAPSHOT locally as an archetype, you can install it locally yourself.

# USAGE:
## install archetype
        $ mvn archetype:create-from-project
        $ cd target/generated-sources/archetype/
        $ mvn clean install

## use archetype
        $ cd /new/dir
        $ mvn archetype:generate \
                -DgroupId=pkg.hello_from_archetype \
                -DartifactId=hello-from-archetype \
                -DarchetypeGroupId=sw.hadoop \
                -DarchetypeArtifactId=hadoop-mr-flat-archetype \
                -DarchetypeVersion=1.1-SNAPSHOT \
                -DinteractiveMode=false

## Enhancements/updates to chapter 5
* force hadoop2 as default
* use mockito
* flatten (per above)

## TODO
* remove hamcrest stuff
* document command-line usage (add `.sh` file to run)
