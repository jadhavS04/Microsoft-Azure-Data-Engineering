# Microsoft-Azure-Data-Engineering
```mermaid
graph TD
    %% Define Color Styles
    classDef source fill:#e1f5fe,stroke:#0288d1,stroke-width:2px;
    classDef lakehouse fill:#e8f5e9,stroke:#2e7d32,stroke-width:3px;
    classDef workload fill:#fff3e0,stroke:#e65100,stroke-width:2px;

    subgraph Sources
        B[Batch Data]:::source
        S[Streaming Data]:::source
    end

    subgraph Lakehouse Storage Layer
        CS[(Cloud Object Storage)]:::lakehouse
        OF[Open Formats: Parquet / Delta]:::lakehouse
        ACID[ACID Transactions & Schema Enforcement]:::lakehouse
        
        CS --- OF
        OF --- ACID
    end

    subgraph Unified Workloads
        SQL[SQL Analytics]:::workload
        DE[Data Engineering]:::workload
        ML[Machine Learning]:::workload
        STR[Streaming]:::workload
    end

    B --> CS
    S --> CS
    
    ACID --> SQL
    ACID --> DE
    ACID --> ML
    ACID --> STR

graph TD
    %% Define Color Styles
    classDef source fill:#e1f5fe,stroke:#0288d1,stroke-width:2px;
    classDef lakehouse fill:#e8f5e9,stroke:#2e7d32,stroke-width:3px;
    classDef workload fill:#fff3e0,stroke:#e65100,stroke-width:2px;

    subgraph Sources
        B[Batch Data]:::source
        S[Streaming Data]:::source
    end

    subgraph Lakehouse Storage Layer
        CS[(Cloud Object Storage)]:::lakehouse
        OF[Open Formats: Parquet / Delta]:::lakehouse
        ACID[ACID Transactions & Schema Enforcement]:::lakehouse
        
        CS --- OF
        OF --- ACID
    end

    subgraph Unified Workloads
        SQL[SQL Analytics]:::workload
        DE[Data Engineering]:::workload
        ML[Machine Learning]:::workload
        STR[Streaming]:::workload
    end

    B --> CS
    S --> CS
    
    ACID --> SQL
    ACID --> DE
    ACID --> ML
    ACID --> STR
    ```
