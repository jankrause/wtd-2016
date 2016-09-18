# Subsituting Operation 

## Description 
A Substituting Operation replaces one or many DESTINATION OBJECTs at a DESTINATION by one or many SOURCE OBJECTs from a SOURCE.
The DESTINATION OBJECTs to replace are defined by a DESTINATION PRIMARY KEY or DESTINATION COMPARISON. The selection of SOURCE OBJECTs 
works analog with SOURCE OBJECT PRIMARY KEYs or SOURCE OBJECT COMPARISONs. This pattern bases on VerbNet exchange-13.6.

## Verbs
barter, change, exchange, replace, substitute, swap, switch, trade

## Also known as
Validator

## Thematic Roles

|  Role                  | Description                                            |Mandatory
|------------------------|--------------------------------------------------------|---------
|DESTINATION             | Where the DESTINATION OBJECTs exist                    | Y
|DESTINATION OBJECT      | What is replaced                                       | Y
|DESTINATION PRIMARY KEY | Identifies the DESTINATION OBJECT uniquely             | N
|DESTINATION COMPARISON  | Identifies the DESTINATION OBJECT                      | N
|SOURCE                  | Origin, where the SOURCE OBJECTs exist                 | Y
|SOURCE OBJECT           | What replaces                                          | Y
|SOURCE PRIMARY KEY      | Identifies the SOURCE OBJECT uniquely                  | N
|SOURCE COMPARISON       | Identifies the SOURCE OBJECT                           | N

## Pattern-specific Rules

|  Role                  | Description                                            
|------------------------|--------------------------------------------------------
|DESTINATION             | always()
|DESTINATION OBJECT      | always()
|DESTINATION PRIMARY KEY | !exists("DESTINATION COMPARISON")
|DESTINATION COMPARISON  | !exists("DESTINATION PRIMARY KEY")
|SOURCE                  | always()
|SOURCE OBJECT           | always()
|SOURCE PRIMARY KEY      | !exists("SOURCE COMPARISON")
|SOURCE COMPARISON       | !exists("SOURCE COMPARISON")

## Example

### Overview

| Property          | Description
|-------------------|--------------------------------------------------------
|Component:         | .NET Framework
|Program:           | String#replace(String, String)
|Version            | 4.5
|Link:              | [https://msdn.microsoft.com/en-us/library](https://msdn.microsoft.com/en-us/library/fk49wtc1(v=vs.110).aspx)
|Description        | Framework for the Windows-platform

### Assignments

|  Role                       | Description                                            
|-----------------------------|--------------------------------------------------------
|DESTINATION                  | The resulting string
|DESTINATION OBJECT           | All occurences of the parameter newValue
|DESTINATION COMPARISON       | The parameter newValue
|SOURCE                       | String (this) 
|SOURCE OBJECT                | All occurences of the parameter oldValue
|SOURCE COMPARISON            | The parameter oldValue
|ERROR SOURCE COMPARISON      | ArgumentNullException (oldValue is null) or ArgumentException (oldValue is empty)
|ERROR DESTINATION COMPARISON | ArgumentNullException (oldValue is null) or ArgumentException (oldValue is empty)
