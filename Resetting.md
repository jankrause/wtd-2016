# Resetting Operation 

## Description 
A resetting operation modifies the ATTRIBUTEs of an OBJECT or the OBJECT itsself in a way, that it equals one of its prior states. The
changed values are taken from a SOURCE.

## Verbs
reset, revert

## Also known as

## Thematic Roles

|  Role            | Description                                             |Mandatory
|------------------|---------------------------------------------------------|---------
|OBJECT            | What is reverted or encapsulates the reverted ATTRIBUTEs| Y
|ATTRIBUTE         | What is reverted                                        | N
|SOURCE            | Where the reverted values are taken from                | Y

## Pattern-specific Rules

|  Role            | Description                                            
|------------------|--------------------------------------------------------
|OBJECT            | always()
|ATTRIBUTE         | hasAttribute("OBJECT")
|SOURCE            | always()

## Example

### Overview

| Property          | Description
|-------------------|--------------------------------------------------------
|Component:         | Java Platform Standard Edition 
|Program:           | java.io.InputStream#reset
|Version            | 8
|Link:              | [docs.oracle.com/javase/8/docs/api](http://docs.oracle.com/javase/8/docs/api/java/io/InputStream.html#reset--)
|Description        | Java Standard Class Library

### Assignments

|  Role            | Description                                            
|------------------|-----------------------------------------------------------------------------
|OBJECT            | InputStream (this)
|ATTRIBUTE         | Byte-position in the InputStream, where reading should start
|SOURCE            | Byte-position, where the operation mark() has been invoked for the last time
