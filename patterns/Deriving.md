# Deriving Operation 

## Description 
A deriving operation derives an OBJECT or a REPORT from a set of ATTRIBUTEs. The derivation is defined by a RULE or ALGORITHM. 

## Verbs
conclude, derive

## Also known as
-

## Thematic Roles

|  Role            | Description                                            |Mandatory
|------------------|--------------------------------------------------------|---------
|ALGORITHM or RULE | Defines the procedure of the derivation                | Y
|OBJECT            | What is derived (a single value)                       | Y
|REPORT            | What is derived (a set of values)                      | Y
|ATTRIBUTE         | Starting points of the derivation                      | Y

## Pattern-specific Rules

|  Role            | Description                                            
|------------------|--------------------------------------------------------
|ALGORITHM         | !exists("RULE")
|RULE              | !exists("ALGORITHM")
|REPORT            | !exists("OBJECT")
|OBJECT            | !exists("REPORT")
|ATTRIBUTE         | always()

## Example

### Overview

| Property          | Description
|-------------------|--------------------------------------------------------
|Component:         | Header-File hukdf.h (Key Derivation Functions (KDFs))
|Program:           | Operation: hu_KDFDerive()
|Version            | Native SDK for BlackBarry 10
|Link:              | [developer.blackberry.com](http://developer.blackberry.com/native/reference/core/com.qnx.doc.crypto.lib_ref/topic/hu_KDFDerive.html?f=hu_KDFDerive)
|Description        | API for Native SDK for BlackBarry 10 smartphones

### Assignments

|  Role            | Description                                            
|------------------|--------------------------------------------------------
|ALGORITHM         | Uses the hash-function specified by parameter ```algid´´´
|REPORT            | The result
|OBJECT            | The key for en- and decryption (parameter ```keyValue´´´)
|ATTRIBUTE         | The parameter ```sharedSecret´´´
|ERROR ALGORITHM   | The result is SB_ERR_KDF_BAD_ALGORITHM (unknown algorithm)
|ERROR ATTRIBUTE   | The result is SB_ERR_NULL_INPUT_BUF (ATTRIBUTE is ```null´´´) or SB_ERR_BAD_INPUT_BUF_LEN (ATTRIBUTE has an invalid length).
|ERROR OBJECT      | The result is SB_ERR_NULL_OUTPUT_BUF (memory of OBJECT is ```null´´´) or SB_ERR_BAD_OUTPUT_BUF_LEN (memory of OBJECT has an invalid length).
