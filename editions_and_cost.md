# Overview 

Snowflake offers multiple editions. Each successive edition builds on the previous edition through the addition of edition-specific features and/or higher levels of service. 
  
* **Standard** - Introductory level
* **Enterprise** - Standard +  Additional features for needs of large-scale enterprises
* **Business Critical**  -  Enterprise + higher data protection for organizations with extremely sensitive data 
* **Virtual Private**  -  Highest level of security

# Editions 

## Standard 

* Introductory level

Features : 

- Complete DWH 
- Automatic data encryption 
- Broad standard for standard and special data types 
- Time travel up to 1 day 
- Disaster recovery for 7 days  beyond time travel 
- Security data share 
- Federated authentification & SSO
- Network policies 
- Premier support 24/7 


Pricing : ... 

## Enterprise 

*  Standard +  Additional features for needs of large-scale enterprises
  
Features :

- All standard features 
- Multi-cluster warehouse 
- Time travel up to 90 days 
- Materialized views 
- Search Optimization 
- Column-level security 
- 24-hour early access to weekly new releases
  
Pricing : 
... 

## Business Critical 
* Enterprise + higher data protection for organizations with extremely sensitive data 

Features : 
- All Enterprise features 
- Additional security features (customer encryption)
- Support for data specific regulation
- Database failover/failback (disaster recovery)

Pricing : 
... 
## Virtual Private 
Highest level of security 

Features : 
 - All the features and services of Business Critical Edition
 - Completely separate Snowflake environment, isolated from all other Snowflake accounts

# 
Pricing : 
... 

<img width="557" alt="Pasted image 20241223231449" src="https://github.com/user-attachments/assets/e2c98002-54cb-4e0b-87d9-5dc046f64bfd" />

# Snowflake Pricing

Compute and Storage costs decoupled 
Pay only what you need 
Scalable and at affordable cloud price 
Pricing depending on the region/cloud provider


Cost is separated in three parts : Compute,  Data Transfer  and Storage 

## Compute Cost 

Compute Cost include : 
- Active warehouse 
- Cloud Services - only charged if exceeds 10% of warehouse consumption 
- Serverless (search optimization, snowpipe) 

Charged for active warehouse per hour 
Billed by second (minimum 1 min)
Depending on the size of the warehouse 

Time / active warehouse / size 
Charged in credits 

![[Pasted image 20241225140402.png]]

![[Pasted image 20241225140307.png]]

## Storage Cost 

- Monthly storage fees 
- Based on average storage used per month 
- Cloud providers 
- Cost calculated after compression 

### On-demande storage 
- Pay only for what you use depending of the region 
- $45/TB

### Capacity Storage 
- Pay only for defined capacity upfront 
- $24.50/TB

## Data Transfer
- Data ingress FREE 
- Data egress CHARGED 
- Cloud Storage Provider


# Links 
https://docs.snowflake.com/en/user-guide/intro-editions
