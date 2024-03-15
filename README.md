# sw-sufficiency-model

```mermaid
erDiagram
    CHILD ||--|| GENDER_IDENTITY : "has a"
    CHILD ||--|| ETHNICITY : "has a"
    CHILD ||--o{ PLACEMENT : "has a"
    PLACEMENT ||--|| PROVIDER : "has a"
    PLACEMENT ||--|| PLACEMENT_TYPE: "has a"
    PLACEMENT ||--|| REFERRAL : "linked to"
    CHILD ||--|{ REFERRAL : "linked to"
    REFERRAL ||--o{ IMPORTANT_LOCATION : "has a"
    REFERRAL ||--o{ NEEDS : "has a"
    CHILD {
        string id PK
        string first_name
        string last_name
        int age
        int siblings
    }
    ETHNICITY {
        int id PK
        string value
    }
    GENDER_IDENTITY {
        int id PK
        string value
    }
    PLACEMENT {
        string id PK
        date placement_date
        string placement_location
        string placement_type
        string school_location
        string placement_name
    }
    PROVIDER {
        string id PK
        string location
        int budget
        string placement_name
    }
    PLACEMENT_TYPE {
        string id PK
        boolean residential
        boolean other    
    }
    REFERRAL {
        int id PK
        date placement_needed_date
        string placement_location_preferred
        string placement_type_preferred
        date referral_date
    }
    IMPORTANT_LOCATION {
        int id PK
        date referral_date
        string family_location
        string school_location
        string primary_home_location
        string other_location
        string place_of_worship
    }
    NEEDS {
        int id PK
        boolean comms_req
        boolean leanring_needs
        boolean health_needs
        boolean cultural_needs
        boolean sibling_placement
    }
```