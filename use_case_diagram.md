@startuml

usecase "CCTV Camera" as UC1
usecase "AI Traffic Detection System" as UC2

rectangle "AI Traffic Detection System" {
    usecase "Helmet Detection" as UC_H
    usecase "Triple Seat Detection" as UC_TS
    usecase "Truck Detection" as UC_T
}

usecase "Output Generation" as UC_O
usecase "Alerts" as UC_A
usecase "Storage" as UC_S

UC1 --> UC2
UC2 --> UC_H
UC2 --> UC_TS
UC2 --> UC_T
UC2 --> UC_O
UC2 --> UC_A
UC2 --> UC_S

@enduml