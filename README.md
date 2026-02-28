# Microsoft-Azure-Data-Engineering
'''mermaid
graph LR
    subgraph Data Sources
        DB[(Databases)]
        APP[Applications]
        LOG[Logs]
        IOT[IoT / Events]
    end

    subgraph Problem Area: Siloed Storage
        DL[(Data Lake \n - Raw Data \n - Cheap \n - No Governance)]
        DW[(Data Warehouse \n - Structured \n - Expensive \n - BI Focus)]
    end

    subgraph Consumers
        BI[BI Tools \n Data Analysts]
        ML[Data Scientists \n ML Models]
    end

    DB --> DL
    APP --> DL
    LOG --> DL
    IOT --> DL

    DL -->|Complex Pipelines \n Duplication| DW
    
    DW --> BI
    DL -->|Slow ML Workflows| ML

    style DL fill:#f9d0c4,stroke:#333,stroke-width:2px
    style DW fill:#f9d0c4,stroke:#333,stroke-width:2px
'''
