```puml
@startuml

node "Mobile App" as mobile

node "Kubernetes Cluster" {
    component "Service"as service
    node "Node 1" {
        component "Pod Client" as client
        component "Pod A" as poda1
        component "Pod ..." as podb2
    }
    node "Node 2" {
        component "Pod A" as poda2
        component "Pod A" as poda3
        component "Pod ..." as podb1
    }
}

mobile -right-> service: caranya?
client --> service
service --> poda1
service --> poda2
service --> poda3

@enduml
```