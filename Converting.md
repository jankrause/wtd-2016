# Converting Operation 

## Description 
A converting operation transforms an OBJECT from the SOURCE_FORMAT into the DESTINATION_FORMAT by using an INSTRUMENT (e.g. external ressource or program), ALGORITHM or RULE. This category bases on the VerbNet classes convert-26.6.2 and Turn-26.6.1.

## Verbs
get around, change, convert, switch, go back, come around, transform, revert, deform, resort, switch_over, turn, get down, get, metamorphose, 
return, settle down, alter, take, fall, move over, translate, transmute, change_over, shift, mutate,


## Also known as
Converter

## Thematic Roles

|  Role            | Description  c                                                   |Mandatory
|------------------|------------------------------------------------------------------|---------
|ALGORITHM or RULE | Procedure of the transformation.                                 | N
|OBJECT            | What is transformed.                                             | Y
|SOURCE FORMAT     | The OBJECT's structure before the transformation                 | Y
|DESTINATION FORMAT| The OBJECT's structure before the transformation                 | Y
|INSTRUMENT        | External ressource or program, which performs the transformation | N

## Pattern-specific Rules

|  Role            | Description                                            
|------------------|--------------------------------------------------------
|ALGORITHM         | !exists("RULE") && !exists("INSTRUMENT")
|RULE              | !exists("ALGORITHM") && !exists("INSTRUMENT")
|INSTRUMENT        | !exists("ALGORITHM") && !exists("RULE")
|OBJECT            | always()
|SOURCE FORMAT     | always()
|DESTINATION FORMAT| always()

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
