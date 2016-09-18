# Searching Operation 

## Description 
A Searching Operation searches for one or many OBJECTs in a SOURCE. The OBJECTs are identified by a PRIMARY KEY or a COMPARISON. The 
number of returned OBJECTs could be limited by specifying a LIMIT. If a Searching Operation returns many OBJECTs, they could be 
sorted as defined by an ORDERING. The detailed procedure for the search could be specified by an ALGORITHM. This pattern bases
on the VerbNet-classes Search-35.2 und obtain-13.5.2.

## Verbs
accept, accrue, accumulate, acquire, advertise, appropriate, borrow, cadge, collect, comb, dive, drag, dredge, exact, excavate, extract, 
find, get, grab, inherit, obtain, patrol, plumb, probe, prospect, prowl, purchase, quarry, rake, receive, recover, regain, retrieve, 
rifle, scavenge, scour, scout, search, seize, select, shop, sift, snatch, trawl, troll, watch

## Also known as


## Thematic Roles

|  Role            | Description                                               |Mandatory
|------------------|-----------------------------------------------------------|---------
|OBJECT            | What is expected to be found                              | Y
|SOURCE            | Where the operation searches                              | Y
|PRIMARY KEY       | Identifies the OBJECT in the SOURCE uniquely              | Y
|COMPARISON        | Identifies the OBJECT in the SOURCE                       | Y
|LIMIT             | Defines an upper or lower threshold for the found OBJECTs | N
|ORDERING          | Defines the sequence of OBJECTs                           | N
|ALGORITHM         | Defines the detailed procedure when searching             | N

## Pattern-specific Rules

|  Role            | Description                                            
|------------------|--------------------------------------------------------
|OBJECT            | always()
|SOURCE            | always()
|PRIMARY KEY       | !exists("COMPARISON")
|COMPARISON        | !exists("PRIMARY KEY")
|LIMIT             | isPlural("OBJECT")
|ORDERING          | isPlural("OBJECT")
|ALGORITHM         | always()

## Example

### Overview

| Property          | Description
|-------------------|--------------------------------------------------------
|Component:         | Java Platform Standard Edition 
|Program:           | javax.activation.MimetypesFileTypeMap#getContentType
|Version            | 8
|Link:              | [docs.oracle.com/javase/8/docs/api](http://docs.oracle.com/javase/8/docs/api/javax/activation/MimetypesFileTypeMap.html#getContentType-java.io.File-)
|Description        | Java Standard Class Library

### Assignments

|  Role            | Description                                            
|------------------|--------------------------------------------------------
|OBJECT            | The MIME-type of the file-extension specified by parameter f
|SOURCE            | See locations specified in the API-documentation
|COMPARISON        | File-extension of parameter f
|LIMIT             | 1
