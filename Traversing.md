# Traversing Operation 

## Description 
A Traversing Operation visits one or more OBJECTs at a DESTINATION. The visited OBJECTs are selected by matching a PRIMARY KEY
or a COMPARISON. On each OBJECT an ALGORITHM is applied. The result of visiting all OBJECTs can be summarized by a REPORT. This
pattern bases on VerbNet-class swarm-47.5.1.

## Verbs
abound, bustle, crawl, creep, hop, iterate, run, swarm, swim, teem, throng, traverse, visit

## Also known as
Visitor-Design Pattern

## Thematic Roles

|  Role            | Description                                            |Mandatory
|------------------|--------------------------------------------------------|---------
|OBJECT            | What is visited                                        | Y
|DESTINATION       | Where the OBJECT exists                                | Y
|COMPARISON        | Identifies the OBJECT                                  | N
|PRIMARY KEY       | Identifies the OBJECT to check uniquely                | N
|ALGORITHM         | Is applied to each visited OBJECT                      | Y
|REPORT            | Summarizes the result of the visits                    | M


## Pattern-specific Rules

|  Role            | Description                                            
|------------------|--------------------------------------------------------
|OBJECT            | always()
|DESTINATION       | always()
|COMPARISON        | !exists("PRIMARY KEY")
|PRIMARY KEY       | !exists("COMPARISON")
|ALGORITHM         | always()
|REPORT            | always()

## Example

### Overview

| Property          | Description
|-------------------|--------------------------------------------------------
|Component:         | JBoss ModeShape Public API
|Program:           | org.modeshape.graph.query.model.Visitors#visitAll
|Version            | 4.5
|Link:              | [docs.jboss.org/modeshape/2.1.0.Final/api](http://docs.jboss.org/modeshape/2.1.0.Final/api/org/modeshape/graph/query/model/Visitors.html#visitAll(org.modeshape.graph.query.model.Visitable, StrategyVisitor))
|Description        | File-archive, which complies with standard JSR-283

### Assignments

|  Role            | Description                                            
|------------------|--------------------------------------------------------
|OBJECT            | Node visitable (given parameter) and all child-nodes
|DESTINATION       | Node visitable
|COMPARISON        | All reachable nodes
|ALGORITHM         | Parameter strategyVisitor
|REPORT            | Depends on the implementation of strategyVisitor
