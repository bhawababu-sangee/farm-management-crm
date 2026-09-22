# ER Diagram - Farm Management CRM

## Relationship Overview

### Farmer / Contact (One) -> Farm (Many)
One farmer can own many farms

### Farm (One) -> Crop (Many)
One farm can have many crops

### Crop (One) -> Harvest (Many)
One crop can have many harvest records

## Diagram Structure

[Contact - Farmer]
      |
      | owns
      v
[Farm__c] 
- Farm_Name__c
- Location__c
- Area_Acres__c
- Status__c
      |
      | contains
      v
[Crop__c]
- Crop_Name__c
- Season__c
- Planting_Date__c
- Expected_Harvest_Date__c
      |
      | yields
      v
[Harvest__c]
- Harvest_Date__c
- Quantity_kg__c
- Quality__c
- Total_Revenue__c

## Notation
Farmer ||--o{ Farm : owns
Farm ||--o{ Crop : contains
Crop ||--o{ Harvest : yields

## Dashboard
Farm Dashboard shows total farms, total crops, total harvest quantity