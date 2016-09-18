# Merging Operation 

## Description 
A merging operation combines at least two OBJECTs or specific of their ATTRIBUTEs. The combination is defined by a RULE or an ALGORITHM. The combined result could be stored at a DESTINATION. The considered OBJECTs could be limited by specifying a LIMIT, a COMPARISON or a PRIMARY KEY. This pattern bases on the VerbNet-class mix-22.1.

## Verbs
add, admix, amalgamate, blend, coalesce, combine, commingle, compound, connect, consolidate, cream, fuse, intermix, join, link, meld, merge, mingle, mix, network, pair, pool, scramble, tie, tumble, unite

## Also known as

## Thematic Roles

|  Role            | Description                                               |Mandatory
|------------------|-----------------------------------------------------------|---------
|OBJECT            | What is combined                                          | Y
|ATTRIBUTE         | Not required                                              | N
|SOURCE            | Where the merged OBJECTs are located before the merger    | Y
|RULE              | Defines how the merger is performed                       | Y
|ALGORITHM         | Many RULEs, which define how the merger is performed      | Y
|DESTINATION       | Where the OBJECTs are stored after the merger             | N
|LIMIT             | Limits the considered OBJECTs (by min. or max. count)     | N
|COMPARISON        | Limits the considered OBJECTs (by a non-unique criterion) | N
|PRIMARY KEY       | Limits the considered OBJECTs (by a unique criterion)     | N

## Pattern-specific Rules

|  Role            | Description                                            
|------------------|--------------------------------------------------------
|OBJECT            | always()
|SOURCE            | always()
|ATTRIBUTE         | hasAttributes("OBJECT")
|ALGORITHM         | !exists("RULE")
|RULE              | !exists("ALGORITHM")
|DESTINATION       | always()
|LIMIT             | !exists("COMPARISON") && !exists("PRIMARY KEY")
|COMPARISON        | !exists("LIMIT") && !exists("PRIMARY KEY")
|PRIMARY KEY       | !exists("COMPARISON") && !exists("LIMIT")

## Example

### Overview

| Property          | Description
|-------------------|--------------------------------------------------------
|Component:         | Ruby Language
|Program:           | Array#join
|Version            | 2.2.0
|Link:              | [https://ruby-doc.org/core-2.2.0/](https://ruby-doc.org/core-2.2.0/Array.html#method-i-join)
|Description        | Ruby Standard Class Library

### Assignments

|  Role             | Description                                            
|-------------------|--------------------------------------------------------
|OBJECT             | The elements of the array
|SOURCE             | The array on which this operation is invoked.
|ATTRIBUTE          | hasAttributes("OBJECT")
|ALGORITHM          | Convert each array-element to a String (starting with index 0) and concat them. If the optional parameter separator is set, put it's value in between two concatenated strings.
|RULE               | Not required
|DESTINATION        | The result
|LIMIT              | Not required
|COMPARISON         | All elements of the array
|PRIMARY KEY        | Not required
