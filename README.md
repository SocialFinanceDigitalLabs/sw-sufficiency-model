# sw-sufficiency-model

#### This entity relationship diagram (ERD) represents the proposed data collection method for the Southwest Sufficiency Project, which aims to standardize children's data collection across the region. Additionally, this ERD can serve as a framework to link with data collected by other local authorities, fostering collaboration and consistency in data management practices across the region.

```mermaid
erDiagram
    CHILD ||--o{ PLACEMENT : "has a"
    PLACEMENT ||--|| PLACEMENT_TYPE: "has a"
    REFERRAL ||--|| PLACEMENT : "linked to"
    CHILD ||--|{ REFERRAL : "linked to"
    REFERRAL ||--o{ IMPORTANT_LOCATION : "has a"
    PLACEMENT ||--o{ NEEDS : "has a"
    PLACEMENT ||--o{ RISKS : "has a"
    PLACEMENT ||--|| FINANCE : "linked to"
    CHILD {
        string id PK
        string local_identifier
    }
    PLACEMENT {
        string id PK
        string placement_location
        categorical placement_type
    }
    PLACEMENT_TYPE {
        string id PK
        boolean foster_care
        boolean residential_care
        boolean supported_home
        boolean adult_support_ratio
    }
    REFERRAL {
        int id PK
        date placement_needed_date
        string placement_location_preferred
        string placement_type_preferred
        categorical planned_or_emergency_placement
        date referral_date
    }
    IMPORTANT_LOCATION {
        int id PK
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
