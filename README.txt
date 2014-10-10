Cref: 
http://localhost:18080/MavenTipsTricks#creating_your_own_archetype

This is a simple maven project based on ch05 of 3rd edition of "Hadoop: The Definitive Guide".

This project is purposed to be built as an archetype, which can be used to
 bootstrap other hadoop-mr projects. Please note that I had to "flatten"
 the maven project structure (hadoop-book uses maven submodules, which
 "mvn archetype:create-from-project" apparently doesn't play well with).

Although I've installed 1.0-SNAPSHOT locally as an archetype, you can do it yourself
 by picking up the "generate archetype" steps at step #5 -- viz.,
        $ mvn archetype:create-from-project


-swhitney, 10 oct 2014.
