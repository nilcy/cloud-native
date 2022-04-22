# cloud-native

Cloud native technologies empower organizations to build and run scalable applications in modern, dynamic environments such as public, private, and hybrid clouds. Containers, service meshes, microservices, immutable infrastructure, and declarative APIs exemplify this approach.

# アーキテクチャ

Client - Gateway -\* Services

```plantuml
@startuml
skinparam monochrome true
skinparam defaultFontName "Yu Gothic UI, sans-serif"
actor User
component Client
component Gateway
component Service
database DB
User - Client : React
Client - Gateway : SuperGraph
Gateway - Service : SubGraph
Service - DB
@enduml
```
