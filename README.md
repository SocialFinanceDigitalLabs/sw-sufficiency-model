# sw-sufficiency-model

```mermaid
erDiagram
    CHILD ||--|| GENDER_IDENTITY : "has a"
    CHILD ||--|| ETHNICITY : "has a"
    CHILD ||--o{ PLACEMENT : "has a"
    PLACEMENT ||--|| PROVIDER : "has a"
    PLACEMENT ||--|| PLACEMENT_TYPE: "has a"
    REFERRAL ||--|| PLACEMENT : "linked to"
    CHILD ||--|{ REFERRAL : "linked to"
    REFERRAL ||--o{ IMPORTANT_LOCATION : "has a"
    PLACEMENT ||--o{ NEEDS : "has a"
    PLACEMENT ||--o{ RISKS : "has a"
    PLACEMENT ||--|| FINANCE : "linked to"
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
        date latest_placement_date
        string placement_location
        categorical placement_type
        string school_location
        string placement_name
        categorical planned_or_emergency_placement
    }
    PLACEMENT_TYPE {
        string id PK
        boolean foster_care
        boolean residentail_care
        boolean supported_home
        boolean adult_support_ratio
    }
    PROVIDER {
        string id PK
        string location
        int budget
        string placement_name
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
        string preferred_home_location
        string other_location
        string location_to_avoid
        string place_of_worship
    }
    NEEDS {
        int id PK
        categorical learning_comms_req
        boolean adaptation_to_home
        boolean cultural_needs
        boolean sibling_placement
    }

    RISKS {
        int id PK
        boolean risk_to_child_sexual_exploitation
        boolean risk_to_child_self_harm
        boolean risk_to_child_criminal_exploitation
        boolean risk_to_child_drugs_alcohol
        boolean risk_to_child_eating_disorder
        boolean risk_to_child_going_missing
        string risk_to_child_specify
        boolean risk_to_others_physical_harm
        boolean risk_to_others_sexual_harm
        boolean risk_to_others_fire_setting
        boolean risk_to_others_harm_animals
        boolean risk_to_others_criminal_exploitation
        string risk_to_others_specify
    }
    FINANCE {
        string id PK
        int total_planned_weekly_cost
    }
```
