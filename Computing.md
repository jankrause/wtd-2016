# Computing Operation 

## Description 
A computing operation derives an OBJECT by applying a mathematical FORMULA. The FORMULA uses at least one OPERAND. In case of many resulting OBJECTs, they can be sorted due to an ORDERING. This pattern bases on the VerbNet-class multiply-108. 

If the computation follows a RULE or an ALGORITHM, the considered operation has to be classified as [deriving operation](Deriving.md).

## Verbs
add, average, calculate, compute, count, deduct, divide, extrapolate, factor out, interpolate, multiply, subtract, sum, tally

## Also known as

## Thematic Roles

|  Role            | Description                                            |Mandatory
|------------------|--------------------------------------------------------|---------
|OBJECT            | The name of the computed value(s)                      | Y
|FORMULA           | The mathematical definition of the OBJECTs computation | Y
|OPERAND           | A value used by the FORMULA                            | Y
|ORDERING          | The sorting of many OBJECTs                            | N

## Pattern-specific Rules

|  Role            | Description                                            
|------------------|--------------------------------------------------------
|OBJECT            | always()
|FORMULA           | always()
|OPERAND           | always()
|ORDERING          | isPlural("OBJECT")

## Example

### Overview

| Property          | Description
|-------------------|--------------------------------------------------------
|Component:         | Java Platform Standard Edition
|Program:           | java.math.BigDecimal#devide
|Version            | 8
|Link:              | [http://docs.oracle.com/javase/8/docs/api/](http://docs.oracle.com/javase/8/docs/api/java/math/BigDecimal.html#divide-java.math.BigDecimal-)
|Description        | Java Standard Class Library

### Assignments

|  Role             | Description                                            
|-------------------|--------------------------------------------------------
|OBJECT             | The value of the quotient
|FORMULA            | this / parameter divisor. If the quotient should be rounded, this must be specified by setting the parameter roundingMode.
|OPERAND            | this and parameter divisor
|ORDERING           | Not required
