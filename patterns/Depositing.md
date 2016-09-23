# Depositing Operation 

## Description 
A depositing operation puts an existing OBJECT at a DESTINATION, e.g. a collection or memory. There the OBJECT can be identified by a COMPARISON
or PRIMARY KEY. This pattern bases on the VerbNet-class put-9.1.

In contrast to a [Creating Operation](Creating.md) only deposits the OBJECT, but does not create it.

## Verbs
add, append, arrange, bury, deposit, embed, immerse, implant, insert, install, lodge, mount, move, park, persist, place, plant, position, put, save, set, situate, sling, stash, station, stick, store, stow, superimpose, write

## Also known as
Setter

## Thematic Roles

|  Role            | Description                                            |Mandatory
|------------------|--------------------------------------------------------|---------
|OBJECT            | What is put on the DESTINATION                         | N
|DESTINATION       | Where the OBJECT is put                                | Y
|PRIMARY KEY       | Identifies the OBJECT at the DESTINATION uniquely      | Y
|COMPARISON        | Identifies the OBJECT at the DESTINATION               | Y

## Pattern-specific Rules

|  Role            | Description                                            
|------------------|--------------------------------------------------------
|OBJECT            | always()                         
|DESTINATION       | always()
|PRIMARY KEY       | !exists("COMPARISON")
|COMPARISON        | !exists("PRIMARY KEY")

## Example

### Overview

| Property          | Description
|-------------------|--------------------------------------------------------
|Component:         | Java Platform Standard Edition 
|Program:           | java.util.Map#put
|Version            | 8
|Link:              | [docs.oracle.com/javase/8/docs/api](http://docs.oracle.com/javase/8/docs/api/java/util/Map.html#put-K-V-)
|Description        | Java Standard Class Library

### Assignments

|  Role            | Description                                            
|------------------|--------------------------------------------------------
|OBJECT            | Parameter value
|DESTINATION       | Map (this)
|PRIMARY KEY       | Parameter key
|ERROR OBJECT      | It is possible to save null as value in a Map.
|ERROR PRIMARY KEY | NullPointerException, if the implementation of the Map does not support null-keys or ClassCastException, if the key is not supported by the Map-implementation.
