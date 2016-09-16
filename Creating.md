# Creating Operation 

## Description 
A checking operation checks if one or more OBJECTs pass a test described by one or more ALGORITHMs or RULEs. The OBJECTs are retrieved from a SOURCE. All tested OBJECTs are identified by one or more COMPARISONs or PRIMARY_KEYs. The result of the test is described by a REPORT. This category bases on the VerbNet classes sight-30.2, peer-30.3 and investigate-35.4

## Verbs
model, cause, formulate, generate, store, recreate, improvise, reconstitute, organize, stage, spawn, style, instigate, invent, compose, dig, publish, derive, rebuild, rearrange, engender, kindle, conjure, reorganize, form, lay, coin, mint, contrive, sire, shape, create, spark, concoct, incite, schedule, manufacture, bring_about, set_off, construct, fabricate, provoke, beget, design, synthesize, produce,

## Also known as
Constructor, Factory Method

## Thematic Roles

|  Role            | Description                                            |Mandatory
|------------------|--------------------------------------------------------|---------
|OBJECT            | What is created .                                      | Y
|ATTRIBUTE         | What is assigned to the OBJECT during the creation.    | N
|PRIMARY KEY       | Ambigious identifier of the OBJECT                     | N
|NAME              | Ambigious identifier of the OBJECT                     | N
|DESTINATION       | Where the OBJECT is stored after creation              | Y
|OWNER             | To what the OBJECT belongs to                          | N

## Pattern-specific Rules

|  Role            | Description                                            
|------------------|--------------------------------------------------------
|OBJECT            | always()
|ATTRIBUTE         | always()
|PRIMARY KEY       | !exists("NAME")
|NAME              | !exists("PRIMARY KEY")
|DESTINATION       | always()
|OWNER             | always()

## Example

### Overview

| Property          | Description
|-------------------|--------------------------------------------------------
|Component:         | JFreeChart
|Program:           | org.jfree.chart.ChartFactory# createBarChar
|Version            | 1.0.19
|Link:              | [www.jfree.org/jfreechart/api](http://www.jfree.org/jfreechart/api/javadoc/org/jfree/chart/ChartFactory.html)
|Description        | Java Library for Diagramming

### Assignments

|  Role            | Description                                            
|------------------|--------------------------------------------------------
|DESTINATION       | Not required
|OBJECT            | Created diagram
|PRIMARY KEY       | Not required
|NAME              | Parameter value
|OWNER             | Not required
|ATTRIBUTE         | All parameters
