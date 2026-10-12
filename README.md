# QAmodule6

```mermaid
flowchart LR
    Raw[Raw data] --> Bronze[Bronze]
    Bronze --> Check{Quality check}
    Check -->|Pass| Silver[Silver]
    Check -->|Fail| Quarantine[Quarantine]
    Silver --> Gold[Gold]
```


```mermaid
flowchart LR
    subgraph Bronze[Bronze layer]
        RawSales[Raw sales]
        RawProducts[Raw products]
    end

    subgraph Silver[Silver layer]
        CleanSales[Clean sales]
        CleanProducts[Clean products]
    end

    RawSales --> CleanSales
    RawProducts --> CleanProducts
    ```
