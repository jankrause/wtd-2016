# Parsing Operation 

## Description 
A parsing operation reads ATTRIBUTEs from a SOURCE to create an OBJECT out of them. The OBJECT is initialized with the ATTRIBUTEs. The expected structure of the ATTRIBUTEs at the SOURCE is defined by a FORMAT. An ALGORITHM describes the procedure of reading the ATTRIBUTEs and building the OBJECT. A parsing operation could delegated subtasks to an INSTRUMENT.


## Verbs
parse, read

## Also known as
Parser

## Thematic Roles

|  Role            | Description                                                 |Mandatory
|------------------|-------------------------------------------------------------|---------
|ATTRIBUTE         | What is read from the SOURCE                                | Y
|SOURCE            | From where the ATTRIBUTES are read                          | N
|OBJECT            | What is build from the ATTRIBUTES                           | Y
|FORMAT            | The structure of the ATTRIBUTEs at the SOURCE               | Y
|ALGORITHM         | Defines how the ATTRIBUTEs are read and the OBJECT is build | N
|INSTRUMENT        | External component, which performs delegated subtasks       | Y


## Pattern-specific Rules

|  Role            | Description                                            
|------------------|-----------------
|ATTRIBUTE         | always          
|SOURCE            | always()        
|OBJECT            | always()        
|FORMAT            | always()        
|ALGORITHM         | always()        
|INSTRUMENT        | always()

## Example

### Overview

| Property          | Description
|-------------------|--------------------------------------------------------
|Component:         | Ruby Language
|Program:           | Date#parse
|Version            | 2.2.0
|Link:              | [https://ruby-doc.org/core-2.2.0/](https://ruby-doc.org/stdlib-2.3.1/libdoc/date/rdoc/Date.html#method-c-parse)
|Description        | Ruby Standard Class Library

### Assignments

|  Role             | Description                                            
|-------------------|--------------------------------------------------------
|ATTRIBUTE          | The day, month and year from the optional parameter string
|SOURCE             | The optional parameter string
|OBJECT             | The date encoded in string
|FORMAT             | Not explicitly specified (except in the source code lib/date/format.rb#_parse()). The parameter comp defines, if the year XX should be interpreted as 19XX (true) or 20XX (false, default).
|ALGORITHM          | Not required
|INSTRUMENT         | Method lib/date/format.rb#_parse()
