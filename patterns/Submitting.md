# Submitting Operation 

## Description 
A Submitting Operation informs one or many PARTICIPANTs at one or many DESTINATIONs about an event. The PARTICIPANTs are
identified by a PRIMARY KEY or a COMPARISON. The notification is done by a MESSAGE in a specific FORMAT. The MESSAGE could
be transferred with an INSTRUMENT. A REPORT shows if the MESSAGE could be delivered successfully or not. This pattern bases on
the VerbNet-classes tell-37.2 und send-11.1.

## Verbs
acquaint, advise, airmail, apprise, convey, deliver, dispatch, express, fedex, forward, hand, inform, mail, notify, pass, pass on,
port, post, print, remind, return, send, shift, ship, shunt, slip, smuggle, sneak, tell, transfer, transmit, transport, update, ups,
wire

## Also known as


## Thematic Roles

|  Role            | Description                                            |Mandatory
|------------------|--------------------------------------------------------|---------
|PARTICIPANT       | Who is informed                                        | Y
|DESTINATION       | Where the PARTICIPANT receives the MESSAGE             | Y
|SOURCE            | Where the MESSAGE comes from                           | Y
|PRIMARY KEY       | Identifies the PARTICIPANT in the SOURCE uniquely.     | Y
|COMPARISON        | Identifies the PARTICIPANT in the SOURCE.              | Y
|MESSAGE           | What is send                                           | Y
|FORMAT            | The structure of the MESSAGE                           | Y
|INSTRUMENT        | What transmits the MESSAGE                             | Y
|REPORT            | Summarizes the send-status of the MESSAGE              | Y

## Pattern-specific Rules

|  Role            | Description                                            
|------------------|--------------------------------------------------------
|PARTICIPANT       | always()
|DESTINATION       | always()
|SOURCE            | always()
|PRIMARY KEY       | !exists("COMPARISON")
|COMPARISON        | !exists("PRIMARY KEY")
|MESSAGE           | always()
|FORMAT            | always()
|INSTRUMENT        | always()
|REPORT            | always()

## Example

### Overview

| Property          | Description
|-------------------|--------------------------------------------------------
|Component:         | Java EE 7 Specification APIs
|Program:           | javax.mail.Transport#send(Message)
|Version            | 7
|Link:              | [http://docs.oracle.com/javaee/7/api](http://docs.oracle.com/javaee/7/api/javax/mail/Transport.html#send-javax.mail.Message-)
|Description        | Extended Class Library for Java

### Assignments

|  Role            | Description                                            
|------------------|--------------------------------------------------------
|PARTICIPANT       | Person who owns the e-mail-address behind PRIMARY KEY
|DESTINATION       | E-Mail-inbox of the PARTICIPANT
|SOURCE            | E-Mail-address of the sender, which is set by operation setFrom on the parameter msg
|PRIMARY KEY       | E-Mail-address, which is added to the message via operation addRecipient() on the parameter msg
|MESSAGE           | The parameter msg
|FORMAT            | E-Mail / MIME
|INSTRUMENT        | Implementation-depended
|REPORT            | The mail has been send successfully if not exception occurs.
