# Product

Everything as Code is a gitlab server with pre-configured namespaces, preconfigured projects, and extra software components. 
It is preconfiugred in such way that it also serves as the production backend as well as deleopment backend. 
```plantuml
cloud "Everything as code" as eac{


database git{

}

node Gitlab{

        component webserver{
        }
        component pages{

        }
        component pipeline{
            
        }
}
Gitlab-down-> git
}
node "develop pc" as dev{
        
}
dev-right->eac  

node "enduser pc" as epc{
        
}

epc-->eac  
@enduml
```

Everything as Code provides one wholistic product the facilitates all aspects of software and its development process. 