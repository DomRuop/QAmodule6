# QAmodule6


```mermaid
flowchart LR
    subgraph BRONZE[Bronze layer]
        CSV1[Book loans]
        CSV2[Returns]
        CSV3[Reservations]
        JSON1[Community events]
        JSON2[Attendance]
        UNS1[Survey responses]
        UNS2[Complaints]
        EXC1[Book metadata]
        EXC2[Acquisition records]
    end

    subgraph SILVER[Silver layer]
        S_CSV1[Book loans]
        S_CSV2[Returns]
        S_CSV3[Reservations]
        S_JSON1[Community events]
        S_JSON2[Attendance]
        S_UNS1[Survey responses]
        S_UNS2[Complaints]
        S_EXC1[Book metadata]
        S_EXC2[Acquisition records]
    end

     subgraph GOLD[Gold layer]
        G1[BLA BLA]
        G2[BLA BLA]
    end

    CSV1 --> S_CSV1
    CSV2 --> S_CSV2
    CSV3 --> S_CSV3
    JSON1 --> S_JSON1
    JSON2 --> S_JSON2
    UNS1 --> S_UNS1
    UNS2 --> S_UNS2
    EXC1 --> S_EXC1
    EXC2 --> S_EXC2
    
    
