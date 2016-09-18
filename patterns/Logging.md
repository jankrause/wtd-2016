# Logging Operation 

## Description 
A logging operation stores a MESSAGE at a DESTINATION. This should enable the later review of an action performed by the system. The MESSAGE has a FORMAT and its criticality is expressed by a PRIORITY. 

## Verbs
log

## Also known as
Logger


## Thematic Roles

|  Role            | Description                                            |Mandatory
|------------------|--------------------------------------------------------|---------
|MESSAGE           | The stored log-entry                                   | Y
|DESTINATION       | Where the OBJECT is stored                             | Y
|FORMAT            | The structure of the MESSAGE                           | N
|PRIORITY          | The relevance of the content of the MESSAGE            | Y

## Pattern-specific Rules

|  Role            | Description                                            
|------------------|--------------------------------------------------------
|MESSAGE           | always()
|DESTINATION       | always()
|FORMAT            | always()
|PRIORITY          | always()

## Example

### Overview

| Property          | Description
|-------------------|--------------------------------------------------------
|Component:         | Java Platform Standard Edition
|Program:           | java.util.logging.Logger#log
|Version            | 8
|Link:              | [http://docs.oracle.com/javase/8/docs/api](http://docs.oracle.com/javase/8/docs/api/java/util/logging/Logger.html#log-java.util.logging.Level-java.lang.String-)
|Description        | Java Standard Class Library

### Assignments

|  Role             | Description                                            
|-------------------|--------------------------------------------------------
|MESSAGE            | The parameter msg
|DESTINATION        | The log-file (depends on the configuration in file logging.properties)
|FORMAT             | The structure of the log-message (depends on the configuration in file logging.properties)
|PRIORITY           | The parameter level
