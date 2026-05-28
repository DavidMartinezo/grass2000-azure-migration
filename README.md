# Grass2000 – Azure Migration Project

## 📌 Overview

This project demonstrates the migration of a legacy ASP.NET application to Microsoft Azure.
The application was deployed using Azure App Service and connected to an Azure SQL Database.

The goal was to modernize the deployment by moving from a local/legacy environment to a cloud-based infrastructure.

---

## 🧱 Architecture

```
User → Azure App Service → Azure SQL Database
```

---

## ☁️ Azure Resources Created

* Resource Group: `rg-grass2000-prod-eastus`
* App Service Plan: `asp-grass2000-prod`
* Web App: `grass2000-web`
* Azure SQL Database
* Azure SQL Server

---

## ⚙️ Deployment Steps

### 1. Create Resource Group

```bash
az group create \
  --name rg-grass2000-prod-eastus \
  --location eastus
```

---

### 2. Create App Service Plan

```bash
az appservice plan create \
  --name asp-grass2000-prod \
  --resource-group rg-grass2000-prod-eastus \
  --sku B1
```

---

### 3. Create Web App

```bash
az webapp create \
  -g rg-grass2000-prod-eastus \
  -p asp-grass2000-prod \
  -n grass2000-web
```

---

### 4. Deploy Application

The legacy ASP.NET application was deployed to Azure App Service using a zip file obtained from the published site.

---

### 5. Configure Azure SQL Database

* Created Azure SQL Server
* Created Azure SQL Database
* Configured SQL Authentication
* Configured firewall access

---

### 6. Update Connection String

The application configuration was updated to point to Azure SQL Database.

⚠️ Sensitive values (passwords / secrets) are not included for security reasons.

---

## 🧪 Issues Resolved

* Azure SQL firewall configuration
* SQL authentication connectivity issues
* Connection string formatting
* Legacy application compatibility in Azure App Service
* Deployment configuration issues

---

## 📸 Screenshots

### Resource Group

<img width="1097" height="166" alt="image" src="https://github.com/user-attachments/assets/d98a3037-6350-47a2-bdc7-6c5c2d97e01b" />


### App Service
<img width="1216" height="39" alt="image" src="https://github.com/user-attachments/assets/5c80ef52-0fde-49a4-ac9d-52282e13c54b" />


<img width="1394" height="52" alt="image" src="https://github.com/user-attachments/assets/60a5d8d5-980e-45d1-a781-43b76dcc9e29" />


### Azure SQL Database

<img width="1176" height="65" alt="image" src="https://github.com/user-attachments/assets/45f5123c-51bb-47c7-bcdf-ca79ec412591" />


### Application Running

<img width="1892" height="981" alt="image" src="https://github.com/user-attachments/assets/4dfc3cc7-9703-4e1a-8ac5-f8cf698b09b4" />

### Deployment Success

<img width="679" height="174" alt="image" src="https://github.com/user-attachments/assets/4e76253c-98c4-48e8-9b88-9b8c15986776" />


---

## 🎯 Outcome

The legacy application is now successfully running in Azure with:

* Cloud-hosted infrastructure
* Managed App Service deployment
* Azure SQL Database integration
* Remote accessibility

---

## 🧠 Key Learnings

* Azure App Service deployment lifecycle
* Azure SQL configuration and networking
* Cloud migration of legacy applications
* Troubleshooting deployment and connectivity issues
* Secure handling of configuration settings

---

## 🚀 Technologies Used

* ASP.NET
* Azure App Service
* Azure SQL Database
* Azure CLI
* SQL Server Authentication
