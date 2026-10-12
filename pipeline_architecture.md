# QA module 6
# pipeline architecture


```mermaid
flowchart LR

    subgraph RAW[Ingested raw Data]
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

    subgraph BRONZE[Bronze layer]
        B_CSV1[Book loans]
        B_CSV2[Returns]
        B_CSV3[Reservations]
        B_JSON1[Community events]
        B_JSON2[Attendance]
        B_UNS1[Survey responses]
        B_UNS2[Complaints]
        B_EXC1[Book metadata]
        B_EXC2[Acquisition records]
    end

    subgraph SILVER[Silver layer]
        S_CSV1[Book loans_clean]
        S_CSV2[Returns_clean]
        S_CSV3[Reservations_clean]
        S_JSON1[Community events_clean]
        S_JSON2[Attendance_clean]
        S_UNS1[Survey responses_clean]
        S_UNS2[Complaints_clean]
        S_EXC1[Book metadata_clean]
        S_EXC2[Acquisition records_clean]
    end

     subgraph GOLD[Gold layer]
        G1[data for report]
    end

    CSV1 --> B_CSV1
    CSV2 --> B_CSV2
    CSV3 --> B_CSV3
    JSON1 --> B_JSON1
    JSON2 --> B_JSON2
    UNS1 --> B_UNS1
    UNS2 --> B_UNS2
    EXC1 --> B_EXC1
    EXC2 --> B_EXC2

    B_CSV1 --> S_CSV1
    B_CSV2 --> S_CSV2
    B_CSV3 --> S_CSV3
    B_JSON1 --> S_JSON1
    B_JSON2 --> S_JSON2
    B_UNS1 --> S_UNS1
    B_UNS2 --> S_UNS2
    B_EXC1 --> S_EXC1
    B_EXC2 --> S_EXC2

    S_CSV1 --> G1
    S_JSON1 --> G1
    S_EXC1 --> G1
    
    
