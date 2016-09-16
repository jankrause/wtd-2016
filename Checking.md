# Checking Operation 

## Description 
A checking operation checks if one or more OBJECTs pass a test described by one or more ALGORITHMs or RULEs. The OBJECTs are retrieved from a SOURCE. All tested OBJECTs are identified by one or more COMPARISONs or PRIMARY_KEYs. The result of the test is described by a REPORT. This pattern bases on the VerbNet classes sight-30.2, peer-30.3 and investigate-35.4

## Verbs
examine, attend, test, spy, stare, study, contains, validate, has, spot, eavesdrop, survey, eye, gape, monitor, make_out, watch,
glance, discover, regard, scent, investigate, ransack, canvass, leer, frisk, view, tap, sniff, inspect, explore, raid, scrutinize, perceive, witness, sight, recognize, descry, quiz, gawk, espy, experience, peek, listen, note, look, peer, is, peep, overhear, check,
glare, glimpse, peruse, savor, observe, goggle, gaze, snoop, squint, scan, ogle, riffle,

## Also known as
Validator

## Thematic Roles

|  Role            | Description                                            |Mandatory
|------------------|--------------------------------------------------------|---------
|ALGORITHM or RULE | Defines the test.                                      | Y
|PRIMARY KEY       | Identifies the OBJECT to check uniquely in the SOURCE. | N
|COMPARISON        | Identifies the OBJECT to check in the SOURCE.          | N
|REPORT            | Summarizes the result of the test                      | Y
|OBJECT            | What is tested                                         | Y
|SOURCE            | Where the checked OBJECTs are located                  | Y

## Pattern-specific Rules

|  Role            | Description                                            
|------------------|--------------------------------------------------------
|ALGORITHM         | !exists("RULE")
|RULE              | !exists("ALGORITHM")
|PRIMARY KEY       | !exists("COMPARISON")
|COMPARISON        | !exists("PRIMARY KEY")
|REPORT            | always()
|OBJECT            | always()
|SOURCE            | always()

## Example

### Overview

| Property          | Description
|-------------------|--------------------------------------------------------
|Component:         | Java Platform Standard Edition 
|Program:           | java.xml.validation.Validator#validate
|Version            | 8
|Link:              | [docs.oracle.com/javase/8/docs/api](http://docs.oracle.com/javase/8/docs/api/javax/xml/validation/Validator.html#validate-javax.xml.transform.Source-)
|Description        | Java Standard Class Library

### Assignments

|  Role            | Description                                            
|------------------|--------------------------------------------------------
|ALGORITHM         | Checks if an XML-document matches a given reference grammar.
|PRIMARY KEY       | Not required
|COMPARISON        | The reference grammar is implementation-depended.
|REPORT            | The XML-document matches the grammer if no exception occurs.
|OBJECT            | The content of the XML-document 
|SOURCE            | The given parameter ```source´´´
|ERROR OBJECT      | If the XML-document is invalid, an ```IOException´´´ is thrown
|ERROR SOURCE      | If the given parameter ```source´´´ is ```null´´´, a ```NullPointerException´´´ is thrown
