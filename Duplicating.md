# Duplicating Operation 

## Description 
A duplicating operation creates a copy of an OBJECT. This copy equals the original OBJECT. The OBJECT is read from a SOURCE and stored at a DESTINATION. The structure of the OBJECT is specified by a FORMAT. This pattern bases on the VerbNet-class transcribe-25.4.

## Verbs
chronicle, clone, copy, document, duplicate, film, forge, imitate, microfilm, photocopy, photograph, record, tally, tally up, tape, televise, transcribe, type

## Also known as


## Thematic Roles

|  Role            | Description                                            |Mandatory
|------------------|--------------------------------------------------------|---------
|OBJECT            | What is copied                                         | Y
|SOURCE            | Where the OBJECT is read from                          | N
|DESTINATION       | Where the copy of the OBJECT                           | N
|FORMAT            | The structure of the OBJECT                            | N

## Pattern-specific Rules

|  Role            | Description                                            
|------------------|--------------------------------------------------------
|OBJECT            | always()
|SOURCE            | always()
|DESTINATION       | always()
|FORMAT            | exists("SOURCE") || exists("DESTINATION")

## Example

### Overview

| Property          | Description
|-------------------|--------------------------------------------------------
|Component:         | Commons IO
|Program:           | org.apache.commons.io.FileUtils#copyFile
|Version            | 2.5
|Link:              | [http://commons.apache.org/proper/commons-io/javadocs/api-2.5/](http://commons.apache.org/proper/commons-io/javadocs/api-2.5/org/apache/commons/io/FileUtils.html#copyFile(java.io.File,%20java.io.File))
|Description        | Java-Library for the handling of files

### Assignments

|  Role             | Description                                            
|-------------------|--------------------------------------------------------
|OBJECT             | The content of the copied file
|SOURCE             | The parameter srcFile
|DESTINATION        | The parameter destFile
|FORMAT             | Binary
|ERROR SOURCE       | NullPointerException, if the parameter srcFile is null or IOException, if srcFile is an invalid file
|ERROR DESTINATION  | NullPointerException, if the parameter destFile is null or IOException, if destFile is an invalid file
