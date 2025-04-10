graph LR
    %% Main A-Proxy node
    proxy["A-Proxy System"]
    
    %% Scenario 1: Personalization Research
    subgraph s1 ["Scenario 1: Compare content across user profiles"]
        direction TB
        persona1a["Young Urban User"]
        persona1b["Senior Rural User"]
        scenario1["Personalization Research"] --> website1["Search Results & News Feeds"]
        persona1a --> scenario1
        persona1b --> scenario1
    end
    
    %% Scenario 2: Web Archiving with Context
    subgraph s2["Scenario 2: Preserve context with archives"]
        direction TB
        persona2["German Locale"]
        scenario2["Web Archiving with Context"] --> archive["Archive"]
        persona2 --> scenario2
    end
    
    %% Scenario 3: User Journey Analysis
    subgraph s3["Scenario 3: Track user journeys"]
        direction TB
        scenario3["User Journey Analysis"] --> site1["Site 1"]
        site1 --> site2["Site 2"]
        site2 --> site3["Site 3"]
    end

    %% General Connection to A-Proxy System
    proxy --> s1
    proxy --> s2
    proxy --> s3
    
    %% Styling
    classDef proxy fill:#d3d3d3,stroke:#333,stroke-width:2px
    classDef scenario fill:#b3e0ff,stroke:#333,stroke-width:1px
    classDef persona fill:#d4edda,stroke:#333,stroke-width:1px
    classDef website fill:#fff3cd,stroke:#333,stroke-width:1px
    classDef archive fill:#f8d7da,stroke:#333,stroke-width:1px
    
    class proxy proxy
    class scenario1,scenario2,scenario3 scenario
    class persona1a,persona1b,persona2 persona
    class website1,site1,site2,site3 website
    class archive archive
