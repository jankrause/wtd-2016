# Describing Operation 

## Description 
A describing operation characterizes one or many OBJECTs in a specific manner. The characterization can be done based on one or many 
ATTRIBUTEs of the OBJECT. The OBJECTs are selected by a matching PRIMARY KEY or COMPARISON. The result of an describing operation is a 
REPORT. If the OBJECT belongs to a known SOURCE, its FORMAT at this location can be described. This pattern bases on the VerbNet-class
characterize-29.2.

## Verbs
accept, adopt, bill, cast, certify, characterize, class, classify, conceive, count, define, depict, describe, detail, diagnose, envisage, 
envision, hail, identify, imagine, interpret, judge, know, paint, peg, perceive, picture, pigeonhole, portray, praise, rank, recast, 
recollect, redraw, regard, remember, report, represent, reveal, see, select, specify, stereo- type, take, treat, typecast, view, visualize

## Also known as


## Thematic Roles

|  Role            | Description                                            |Mandatory
|------------------|--------------------------------------------------------|---------
|OBJECT            | What is described.                                     | Y
|ATTRIBUTE         | Property of the OBJECT used for the description.       | Y
|COMPARISON        | Identifies the OBJECT in the SOURCE (not unique).      | N
|PRIMARY KEY       | Identifies the OBJECT in the SOURCE (unique).          | Y
|REPORT            | The description                                        | Y
|SOURCE            | Location, from where the OBJECT is taken               | N
|FORMAT            | The structure of the OBJECT at the SOURCE              | N

## Pattern-specific Rules

|  Role            | Description                                            
|------------------|--------------------------------------------------------
|OBJECT            | always()
|ATTRIBUTE         | hasAttribute("OBJECT")
|COMPARISON        | isPlural("OBJECT") && !exists("PRIMARY KEY")
|PRIMARY KEY       | isPlural("OBJECT") && !exists("COMPARISON")
|REPORT            | always()
|OBJECT            | always()
|SOURCE            | exists("SOURCE")

## Example

### Overview

| Property          | Description
|-------------------|--------------------------------------------------------
|Component:         | MAchine Learning for LanguagE Toolkit (Mallet)
|Program:           | cc.mallet.classify.NaiveBayes# classify
|Version            | 2.0.7
|Link:              | [mallet.cs.umass.edu](http://mallet.cs.umass.edu/api/cc/mallet/classify/NaiveBayes.html)
|Description        | Java-Library for the classification of texts

### Assignments

|  Role      | Description                                            
|------------|--------------------------------------------------------
|OBJECT      | The parameter instance
|ATTRIBUTE   | The components of FeatureVector
|REPORT      | The category into which the vector has been classified
|FORMAT      | Parameter instance

