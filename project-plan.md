# Farm Management CRM - Project Plan

## 1. Project Overview
Farm Management CRM is a Salesforce-based solution to manage Farms, Crops, and Harvests for SkillWallet Group Project.

## 2. Objective
To help farmers and farm owners track their farm activities, crop cycles, and harvest yield using Salesforce CRM.

## 3. Modules
- Farm Management
- Crop Management
- Harvest Management
- Farmer / Worker Management
- Inventory & Equipment

## 4. Salesforce Objects
- Farm__c: Farm_Name__c, Location__c, Area_Acres__c, Owner__c, Status__c
- Crop__c: Crop_Name__c, Farm__c (Master-Detail), Season__c, Planting_Date__c, Expected_Harvest_Date__c
- Harvest__c: Crop__c (Master-Detail), Harvest_Date__c, Quantity_kg__c, Quality__c

## 5. Features
- Dashboard for total farms and yield
- Reports on crop performance
- Automation: Email alert before harvest date

## 6. Team
bhawababu-sangee - Developer & Admin