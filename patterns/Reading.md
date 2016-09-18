# Reading Operation 

## Description 
A reading operation returns one or many OBJECTs from a SOURCE. The position of the OBJECT in the SOURCE is defined by a PRIMARY KEY (e.g. an address, a reference or an index). This category based on VerbNet class get-13.5.1.

If the position of the OBJECT in the SOURCE is not uniquely specified, but found by a matching COMPARISON, then the operation is classified as [Searching.md](searching operation) and not as reading operation.

## Verbs
attain, book, buy, call, cash, catch, charter, choose, conserve, earn, fetch, gain, gather, get, hire, lease, order, phone, pick, pluck, procure, pull, reach, read, rent, reserve, score, secure, shoot, slaughter, steal, vote, win

## Also known as
Accessor, Getter


## Thematic Roles

|  Role            | Description                                            |Mandatory
|------------------|--------------------------------------------------------|---------
|OBJECT            | What is copied                                         | Y
|PRIMARY KEY       | Where the OBJECT is read from                          | Y
|SOURCE            | Where the copy of the OBJECT                           | Y

## Pattern-specific Rules

|  Role            | Description                                            
|------------------|--------------------------------------------------------
|OBJECT            | always()
|PRIMARY KEY       | always()
|SOURCE            | always()

## Example

### Overview

| Property          | Description
|-------------------|--------------------------------------------------------
|Component:         | Commons IO
|Program:           | org.apache.commons.io.FileUtils#readFileToString
|Version            | 2.5
|Link:              | [http://commons.apache.org/proper/commons-io/javadocs/api-2.5/](http://commons.apache.org/proper/commons-io/javadocs/api-2.5/org/apache/commons/io/FileUtils.html#readFileToString(java.io.File,%20java.lang.String))
|Description        | Java-Library for the handling of files

### Assignments

|  Role             | Description                                            
|-------------------|--------------------------------------------------------
|OBJECT             | The file, which is addressed via the parameter file
|PRIMARY KEY        | The local file system
|SOURCE             | The path-property of parameter file
