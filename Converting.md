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
|Component:         | Java Server Faces 
|Program:           | javax.faces.convert.DateTimeConverter# getAsObject
|Version            | 2.2
|Link:              | [javaserverfaces.java.net/docs/2.2](https://javaserverfaces.java.net/docs/2.2/javadocs/javax/faces/convert/DateTimeConverter.html#getAsObject(javax.faces.context.FacesContext, javax.faces.component.UIComponent, java.lang.String))
|Description        | Java-Web-Framework

### Assignments

|  Role            | Description                                            
|------------------|--------------------------------------------------------
|RULE              | Not required
|ALGORITHM         | See algorithm in API-documentation referenced above
|INSTRUMENT        | The attribute locale of the given instance of UIViewRoot
|DESTINATION FORMAT| java.util.Date
|SOURCE FORMAT     | java.lang.String (the specific format must comply with java.text.SimpleFateFormat)
|OBJECT            | The parameter value
|ERROR OBJECT      | If parameter value is null, the operation returns null as result
