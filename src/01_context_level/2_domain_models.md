# Domain model

Figure 2 Domain model
```plantuml 

actor Developer
actor DomainExpert as de
actor Tester

rectangle {
actor "Scrum Master" as sm
actor "Product Owner" as po
actor Architect
	sm-down->po
	po-down->Architect
}
rectangle "Everything as Code" {
usecase ci as "You can use
several lines to define your usecase.
You can also use separators.
--
Several separators are possible.
==
And you can add titles:
..Conclusion..
This allows large description."


(Code)-right-(Model)
(Model)-right-(Test)	
  (ci) <|-up--(Model)
  Code--|>ci
  Test---|>ci

(Process)-down-(Requirement)
(Requirement)-down-(Design)
Requirement-right--|>ci 

(Infrastructure)-down-(Artifact)  
(Infrastructure)-up-(Interface)

Infrastructure-left--|>ci
  ci <|-down-(System)
}
Developer -down--> Code :commits
de -down--> Model :defines
Tester -down-->Test : executes

Architect -left--> Design :maintains
po -left--> Requirement :manages 
sm -left-> Process : facilitates

```
 Process--|>ci 
Design---|>ci
Requirement--->ci
Design-right--->ci


  (ci) <|-(Design)
  (ci) <|-right-(Requirement)
  (ci) <|--(Process)

 

  (ci) <|--left-(Artifact)
  (ci) <|---(Infrastructure)
  (ci) <|-(Interface)


rectangle team{
}
rectangle util{
}




rectangle env{
	actor Installer
	actor Environment
	actor "Production Environment" as pe
	Installer -down-Environment
	Environment -down-pe
}
Environment -right--> Infrastructures: provides
Installer -right--> Artifacts: installs
ProductionEnvironment -right--> System: runs
