# Lead Assignment Automation with Flow & Apex

🚀 Automatically route incoming leads to the correct sales reps based on their country, and fallback to round-robin logic when no match is found.

## 💡 Features
- Auto-assignment via Flow based on region
- Custom Metadata for region-to-user mapping
- Fallback Apex logic for round-robin assignment

## 🧠 Tools Used
- Flow Builder
- Apex
- Custom Metadata

## 🧩 Components
- **Flow**: Record-Triggered on Lead creation
- **Apex**: `LeadAssignmentFallback` class for round-robin logic
- **Custom Metadata**: `LeadAssignmentMapping__mdt`

## 📷 Flow Overview
![flow-overview](https://github.com/user-attachments/assets/7ed81333-1c51-47b2-a4e3-8fffc9cbfe24)

## 📂 How It Works
1. A lead is created.
2. Flow checks `LeadAssignmentMapping__mdt` for a region match.
3. If found, assigns the lead to that user.
4. If not found, an Apex action assigns the lead to the next fallback user in a round-robin manner.

## 📦 Metadata Sample

```csv
DeveloperName,Region__c,UserId__c,Label
USA_Mapping,USA,005XXXXXXX100,USA Mapping
UK_Mapping,UK,005XXXXXXX101,UK Mapping
