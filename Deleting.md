# Deleting Operation 

## Description 
A deleting operation removes one or many OBJECTs permanently from a SOURCE. The OBJECTs to remove are identified by a PRIMARY
KEY, a COMPARISON or a RULE. The number of removed OBJECTs could be limited by specifying a LIMIT. This pattern bases on the 
VerbNet-classes remove-10.1 and destroy-44.

## Verbs
abstract, blitz, cull, decimate, deduct, delete, demolish, depose, destroy, disengage, disfigure, disgorge, dismiss, eject, 
eradicate, excise, expel, extrude, maim, omit, ostracize, oust, pry, reap, remove, retract, separate, sever, subtract, uproot,
withdraw, wreck

## Also known as

## Thematic Roles

|  Role            | Description                                            |Mandatory
|------------------|--------------------------------------------------------|---------
|OBJECT            | What is removed                                        | Y
|SOURCE            | Where the OBJECTs are removed                          | Y
|PRIMAY KEY        | Defines which OBJECT is removed                        | Y
|COMPARISON        | Defines which OBJECTs are removed (simple criteria)    | Y
|RULE              | Defines which OBJECTs are removed (computed thresholds)| Y
|LIMIT             | Min. or max. count of affected OBJECTs                 | Y

## Pattern-specific Rules

|  Role            | Description                                            
|------------------|--------------------------------------------------------
|OBJECT            | always()
|SOURCE            | always()
|PRIMAY KEY        | !exists("COMPARISON") && !exists("RULE")
|COMPARISON        | !exists("PRIMARY KEY") && !exists("RULE")
|RULE              | !exists("COMPARISON") && !exists("PRIMARY KEY")
|LIMIT             | !exists("PRIMARY KEY") 

## Example

### Overview

| Property          | Description
|-------------------|--------------------------------------------------------
|Component:         | jQuery
|Program:           | remove
|Version            | 3.1
|Link:              | [api.jquery.com/](http://api.jquery.com/remove/)
|Description        | Javascript framework for web development

### Assignments

|  Role            | Description                                            
|------------------|--------------------------------------------------------
|OBJECT            | The DOM-objects to delete
|SOURCE            | The DOM-tree
|PRIMAY KEY        | The parameter selector in format of a jQuery-ID-selector
|COMPARISON        | The parameter selector
|RULE              | Deleted are those DOM-objects which matches the parameter selector
