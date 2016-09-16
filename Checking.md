# Checking Operation 

## Description 
A checking operation checks if one or more OBJECTs pass a test described by one or more ALGORITHMs or RULEs. The OBJECTs are retrieved from a SOURCE. All tested OBJECTs are identified by one or more COMPARISONs or PRIMARY_KEYs. The result of the test is described by a REPORT. This category bases on the VerbNet classes sight-30.2, peer-30.3 and investigate-35.4

## Verbs
examine, attend, test, spy, stare, study, contains, validate, has, spot, eavesdrop, survey, eye, gape, monitor, make_out, watch,
glance, discover, regard, scent, investigate, ransack, canvass, leer, frisk, view, tap, sniff, inspect, explore, raid, scrutinize, perceive, witness, sight, recognize, descry, quiz, gawk, espy, experience, peek, listen, note, look, peer, is, peep, overhear, check,
glare, glimpse, peruse, savor, observe, goggle, gaze, snoop, squint, scan, ogle, riffle,

## Also known as
Validator

## Thematic Roles

|  Role            | Description                                            |Mandatory
|------------------|--------------------------------------------------------|---------
|ALGORITHM or RULE | Defines the test.                                      | Y
|PRIMARY KEY       | Identifies the OBJECT to check uniquely in the SOURCE. | N
|COMPARISON        | Identifies the OBJECT to check in the SOURCE.          | N
|REPORT            | Summarizes the result of the test                      | Y
|OBJECT            | What is tested                                         | Y
|SOURCE            | Where the checked OBJECTs are located                  | Y

## Pattern-specific Rules

|  Role            | Description                                            
|------------------|--------------------------------------------------------
|ALGORITHM         | !exists("RULE")
|RULE              | !exists("ALGORITHM")
|PRIMARY KEY       | !exists("COMPARISON")
|COMPARISON        | !exists("PRIMARY KEY")
|REPORT            | always()
|OBJECT            | always()
|SOURCE            | always()
