# Context Level


```plantuml
@startuml

rectangle "Everything as Code" {
  (ci) <|-up-(code)
  (ci) <|-up-(model)
  (ci) <|-up-(tests)
  (ci) <|-right-(designs)
  (ci) <|-right-(Requirements)
  (ci) <|-right-(interfaces)
  (ci) <|-left-(processes)
  (ci) <|--left-(artifacts)
  (ci) <|--left-(infrastructures)
  (ci) <|-down-(system)
}

@enduml
```

everything within a software project can be threated as code.

code has the following properties:

it can be reverted
it can be validated
it can be check for varous non-functional properties
it is text based( human readable)
it has strong syntax
it has  semantic meanings
it can be compiled to a machine langange
