# Domain model

Figure 2 Stakeholders
```plantuml 

rectangle team1{
actor Developer
actor Tester
actor DomainExpert as de
Developer -down-Tester
Tester-down-de
}

rectangle team2{
	actor Installer
	actor Environment
	actor "Production Environment" as pe
	Installer -down-Environment
	Environment -down-pe

}
rectangle team3{
    actor Architect
    actor "Product Owner" as po
	actor Integrator
	Architect -down->po
	po-down->Integrator
}

```
