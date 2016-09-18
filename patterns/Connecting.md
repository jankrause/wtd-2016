# Connecting Operation 

## Description 
Establishes a connection between a SOURCE and a DESTINATION. The connection can be used by at least two PARTICIPANTs. The PARTICIPANTs communicate in a specific FORMAT (e.g. a protocol). The PARTICIPANTs can be addressed by a PRIMARY KEY or a COMPARISON. The connection is closed after running out a TIME TO LIVE. This pattern bases on the VerbNet-class establish-55.5.  


## Verbs
arrange, bring about, connect, constitute, devise, establish, fake, feign, format, found, implement, initiate, innovate, instigate, institute, introduce, launch, machinate, mount, open, open up, organize, originate, pioneer, plant, prepare, simulate, stage, strike up, synthesise

## Also known as
Connector


## Thematic Roles

|  Role            | Description                                               |Mandatory
|------------------|-----------------------------------------------------------|---------
|SOURCE            | The origin of the established connection                  | N
|DESTINATION       | Where the established connection points to                | Y
|PARTICIPANT       | What is copied                                            | N
|FORMAT            | The structure of the data interchanged via the connection | N
|PRIMARY KEY       | Identifies one PARTICIPANT uniquely                       | N
|COMPARISON        | Identifies one or many PARTICIPANTs                       | N
|TIME TO LIVE      | The maximum age of an established connection              | N

## Pattern-specific Rules

|  Role            | Description                                            
|------------------|--------------------------------------------------------
|SOURCE            | always()
|DESTINATION       | always()
|PARTICIPANT       | exists("DESTINATION")
|FORMAT            | always()
|PRIMARY KEY       | exists("PARTICIPANT") && !exists("COMPARISON")
|COMPARISON        | exists("PARTICIPANT") && !exists("PRIMARY KEY")
|TIME TO LIVE      | always()

## Example

### Overview

| Property          | Description
|-------------------|-------------------------------------------------------------------------------------------------------------
|Component:         | The Python Standard Library
|Program:           | socket#createConnection
|Version            | 2.7
|Link:              | [https://docs.python.org/2/library/](https://docs.python.org/2/library/socket.html#socket.create_connection)
|Description        | Standard class-library for Python

### Assignments

|  Role             | Description                                            
|-------------------|-----------------------------------------------------------------------
|SOURCE             | The optional parameter source_address (a tuple of IP-address and port)
|DESTINATION        | The parameter address (a tuple of IP-address and port)
|PARTICIPANT        | The processes listening at SOURCE and DESTINATION
|FORMAT             | Transmission Control Protocol (TCP)
|PRIMARY KEY        | IP- and port-combination of SOURCE and DESTINATION
|TIME TO LIVE       | The optional parameter timeout (in seconds)
