# Salesforce Implementation Details

## Custom Objects Created

### 1. Farm Object (Farm__c)
- Farm_Name__c (Text)
- Location__c (Text)
- Area_Acres__c (Number)
- Owner__c (Lookup to Contact)
- Status__c (Picklist: Active, Inactive)

### 2. Crop Object (Crop__c)
- Crop_Name__c (Text)
- Farm__c (Master-Detail to Farm__c)
- Season__c (Picklist: Kharif, Rabi, Summer)
- Planting_Date__c (Date)
- Expected_Harvest_Date__c (Date)

### 3. Harvest Object (Harvest__c)
- Crop__c (Master-Detail to Crop__c)
- Harvest_Date__c (Date)
- Quantity_kg__c (Number)
- Quality__c (Picklist: A, B, C)
- Market_Price__c (Currency)
- Total_Revenue__c (Formula: Quantity_kg__c * Market_Price__c)

## Flows Implemented
1. Auto-create Harvest record when Crop status = Ready for Harvest
2. Send email to Farm Owner 7 days before Expected Harvest Date

## Validation Rules
1. Area_Acres__c > 0
2. Expected_Harvest_Date__c > Planting_Date__c

## Reports & Dashboards
- Total Yield per Farm - Bar Chart
- Crop-wise Revenue - Pie Chart
- Harvest Quality Report