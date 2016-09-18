# Initiating Operation 

## Description 
A Initiating Operation starts one or more ACTIONs. The duration of each ACTION can be limited with a TIME TO LIVE. This pattern bases 
on the VerbNet-class begin-55.1.

## Verbs
begin, commence, go on, notify, pledge, proceed, recommence, resume, start, start off, trigger, undertake, update

## Also known as
Trigger

## Thematic Roles

|  Role            | Description                                            |Mandatory
|------------------|--------------------------------------------------------|---------
|ACTION            | What is started                                        | Y
|TIME TO LIVE      | The maximum duration of an ACTION                      | Y

## Pattern-specific Rules

|  Role            | Description                                            
|------------------|--------------------------------------------------------
|ACTION            | always()
|TIME TO LIVE      | always()

## Example

### Overview

| Property          | Description
|-------------------|--------------------------------------------------------
|Component:         | jQuery
|Program:           | trigger
|Version            | 3.1
|Link:              | [api.jquery.com](http://api.jquery.com/trigger/)
|Description        | Javascript framework for web development

### Assignments

|  Role            | Description                                            
|------------------|--------------------------------------------------------
|ACTION            | Launches the event-handlers with type eventHandler on the corresponding DOM-element
