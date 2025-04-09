# A-Proxy Demo Scenarios

```mermaid
graph TD
    %% Main A-Proxy node
    proxy[A-Proxy System]
    
    %% Scenario 1: Personalization Research
    scenario1[Personalization Research]
    persona1a[Young Urban User]
    persona1b[Senior Rural User]
    website1[Search Results & News Feeds]
    
    %% Scenario 2: Web Archiving with Context
    scenario2[Web Archiving with Context]
    persona2[German Locale]
    archive[(Archive)]
    
    %% Scenario 3: User Journey Analysis
    scenario3[User Journey Analysis]
    site1[Site 1]
    site2[Site 2]
    site3[Site 3]
    
    %% Connections for Scenario 1
    proxy --> scenario1
    persona1a --> scenario1
    persona1b --> scenario1
    scenario1 --> website1
    
    %% Connections for Scenario 2
    proxy --> scenario2
    persona2 --> scenario2
    scenario2 --> archive
    
    %% Connections for Scenario 3
    proxy --> scenario3
    scenario3 --> site1
    site1 --> site2
    site2 --> site3
    
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

    %% Labels
    subgraph "Scenario 1: Compare content across user profiles"
        scenario1
        persona1a
        persona1b
        website1
    end
    
    subgraph "Scenario 2: Preserve context with archives"
        scenario2
        persona2
        archive
    end
    
    subgraph "Scenario 3: Track user journeys"
        scenario3
        site1
        site2
        site3
    end
```

## Diagram Description

This diagram illustrates the three primary demonstration scenarios for A-Proxy:

1. **Personalization Research**: Shows how different user profiles (young urban user vs. senior rural user) receive different content when accessing the same websites. This demonstrates how A-Proxy can be used to systematically investigate content personalization across platforms.

2. **Web Archiving with Context**: Illustrates how A-Proxy creates contextualized web archives that preserve not just the page content but also the persona context (e.g., German locale) that generated that view. This addresses a significant gap in current web archiving methodologies.

3. **User Journey Analysis**: Demonstrates A-Proxy's ability to record sequences of web interactions under consistent persona settings. This functionality allows researchers to analyze conversion pathways, content discovery patterns, and information-seeking behaviors across multiple sites.

The central A-Proxy system connects to all three scenarios, highlighting its versatility as a research, archiving, and analysis tool.
