# mowitnow, Xebia test project

##Code status
* Built with jdk8 : [![Build Status](https://travis-ci.org/Eaque/mowitnow.svg?branch=master)](https://travis-ci.org/Eaque/mowitnow)
* [![Coverage Status](https://coveralls.io/repos/Eaque/mowitnow/badge.svg)](https://coveralls.io/r/Eaque/mowitnow)

##Goal
Write a program which, from a file (or a stream), simulates lawnmowers and their moves on a lawn.
The file (or stream) contains data representing the size of the lawn, the position and the direction of a set of lawnmowers. 

#Build
Run `mvn clean install`

###Continuous integration
You can use tools such as Jenkins to integrate and deploy continuously.

##Test
Run `mvn test`

##Usage
* As a standalone program :
  * `java -jar mowitnow-1.0.0.jar < (file or stream)`
  * `java -jar mowitnow-1.0.0.jar fileName`
* As a jar library :
  * Use one of the method **createLawn** of the class **LawnCreator** : `LawnCreator.createLawn(file)`

##Functional choices (disambiguation)

* All the lawnmowers are placed on the lawn at the same time (initial time). 
* When a lawnmower meets another one, nothing happens when it tries to move, and then the lawnmower runs the next command. The same behavior applies when the lawnmowers gets out of bounds.
* Available commands are 'A', 'G' and 'D'. Any other character than those ones are ignored.

##Todos

* Internationalization (I18N).
* Change, or use a second code coverage tool. Currently, coveralls does not support Java 8. JaCoCo for example, supports Java 8.