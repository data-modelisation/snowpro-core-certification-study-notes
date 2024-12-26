# Access Control
Access Control is based on main two aspects **Discretonary (DAC)**  and **Role-based Access Control (RBAC)**. 

**Discretonary (DAC)** is an *identity-based access control model that gives users some control over their data*.
- Each object has an owner. 
- Owner can grant access to that object

**Role-based Access Control (RBAC)**
Privileges -> Roles -> Users

Every object is owned by one single role OWNERSHIP privileges 
Ownership can be transferred 


# Role Hierarchy 
![Pasted image 20241226173123](https://github.com/user-attachments/assets/5814476a-e562-4df2-9527-31430af34bec)

Roles are assigned to user 
Multiple roles can be assigned 

## System-defined Roles 

Can't be dropped 
Privileges can be added but not revoked 

**ORGADMIN** 
Manages actions on organizational level 
- Create accounts 
- View all accounts 
- View account usage information 
-
**ACOUNTADMIN** 
Top-level role 
* Should be to limited bumber of users 
* Contains SECURITYADMIN & SYSADMIN
* Can manage all objects in account 
* Inc share and reader account 
* Modify account-level parameters 
* Manage billing & resource monitors 

**SECURITYADMIN** 
Manage any object grant globally 
* MANAGE GRANTS privilege 
* Create, monitor and manage users & roles 
* Inherits USERADMIN privileges 

**SYSADMIN** 
Create warehouses, databases & other objects
- All custom roles should be assigned to
- Can grant privileges on warehouses, databases, and other objects. 

**USERADMIN**
Dedicated to user and role management 
* CREATE USER & CREATE ROLE privileges 
* Can manage users and roles that are owned 

**PUBLIC** 
Automatically granted per default 

**CUSTOME ROLE** 
Created by USERADMIN or higher 
* CREATE ROLE privilege 
* Should be assigned to SYSADMIN (otherwise, SYSADMIN won't be able to manage objects created by these roles)
* Custom database roles can be created by owner 
