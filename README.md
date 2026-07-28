<p align="center">
  <img width="474" height="279" alt="image" src="https://github.com/user-attachments/assets/584155f5-b617-48f1-bd7c-22029abedfb7" />
</p>

# Entra ID Tenant Setup & Configuration

This project demonstrates the foundational configuration of a Microsoft Entra ID tenant from the ground up, simulating the initial setup responsibilities of an IAM Analyst or Identity Engineer in an enterprise environment. Starting with tenant properties and brand customization, the lab walks through building a cloud-native Entra ID tenant for the fictional company, Kennon Technologies, including sign-in branding, privacy statement configuration, licensing verification, manual and bulk user provisioning, and initial security and Microsoft 365 group creation. All configurations are hands-on in a live Microsoft Entra ID tenant and reflect real-world IAM practices around tenant governance, identity provisioning, and directory administration. The lab serves as the foundational layer for subsequent Entra ID labs covering RBAC, Conditional Access, Privileged Identity Management, and enterprise SSO.

---

## Prerequisites

This is the first lab of the [Entra ID Lab Series](https://github.com/RyanKennon/Entra-ID-Lab-Series/tree/main).
The following are required before starting the series:

- **Microsoft Entra ID Tenant** — Sign up for a free Entra ID tenant/trial at [entra.microsoft.com](https://entra.microsoft.com)
- **Microsoft Entra ID P1 or P2 License** — Required for Custom Branding features to apply; a free 30-day trial is available under Billing → Licenses → Try/Buy
- **GitHub Account** — Required to follow along with lab documentation and host your own portfolio

---

## Environments and Technologies Used

- Microsoft Entra ID (Cloud-Native Tenant)
- Microsoft Entra Admin Center
- Microsoft Entra ID Custom Branding
- Microsoft Entra ID Bulk Operations
- Microsoft Entra ID Security & Microsoft 365 Groups
- GitHub (Asset Hosting)

---

## Table of Contents

- [1) Tenant Properties](#1-tenant-properties)
- [2) Company Branding](#2-company-branding)
- [3) Privacy Statement](#3-privacy-statement)
- [4) Manual User Creation](#4-manual-user-creation)
- [5) Bulk User Creation](#5-bulk-user-creation)
- [6) Security Group Creation](#6-security-group-creation)
- [7) Microsoft 365 Group Creation](#7-microsoft-365-group-creation)

---

### 1) Tenant Properties

Tenant properties establish the foundational identity of the Entra ID tenant, including the organization name and technical contact information. These settings appear across the admin center and help distinguish the tenant as belonging to Kennon Technologies rather than a generic default tenant.

1. In the **Entra ID** dropdown then select **Overview**
2. For the **Name** enter **Kennon Technologies** then **Save**

<p align="center">
  <img width="709" height="373" alt="image" src="https://github.com/user-attachments/assets/e14a37df-084e-4d65-99a8-bc70f29875b2" />
</p>

---

### 2) Company Branding

Company branding customizes the visual identity of the sign-in experience by applying a custom favicon, background image, and page background color. This ensures users interact with a sign-in page that reflects Kennon Technologies rather than Microsoft's default Entra ID branding.

1. In the **Entra ID** dropdown select **Company Branding** then select **Customize**
2. For the **Favicon** enter [**Kennon Technologies Favicon**](https://raw.githubusercontent.com/RyanKennon/Entra-Tenet-Setup/main/KT%20Favicon.jpg)
3. For the **Background Image** enter [**Kennon Technologies Background Logo**](https://raw.githubusercontent.com/RyanKennon/Entra-Tenet-Setup/main/Kennon%20Technologies%20Logo.png)
4. For the **Page Background Color** enter **1800ad** for the **Hex**
5. **Review + Create** then **Create**

<p align="center">
  <img width="331" height="164" alt="image" src="https://github.com/user-attachments/assets/1fd37dab-c270-4e30-ba5c-8b27228ef446" />
</p>

---

### 3) Privacy Statement

Publishing a privacy statement link in the sign-in footer provides users with visibility into how their identity data is collected and used. This is a standard governance practice for production tenants and demonstrates awareness of privacy/compliance requirements in an IAM context.

1. In the **Entra ID** dropdown select **Company Branding** then select **Layout**
2. Under **Default Sign-In Experience** Select **Edit**
3. Open the **Footer** page then upload the following information:
   - **Display Text:** Privacy Statement
   - **URL:** https://github.com/RyanKennon/Entra-Tenet-Setup/blob/main/privacy-statement
4. **Review + Save** then **Save**

<p align="center">
  <img width="483" height="329" alt="image" src="https://github.com/user-attachments/assets/e9bc5f95-8de8-4832-b511-4c753c552f37" />
</p>

---

### 4) Manual User Creation

Manually creating a user identity demonstrates the standard single-user provisioning workflow available in the Entra admin center. This establishes a baseline understanding of user attributes and account configuration before moving to bulk provisioning at scale.

1. In the **Entra ID** dropdown select **Users** then **All Users**
2. Select **+ New User** then **Create New User**
3. On the **Basics** tab enter the following information:
   - **User Principal Name:** johnsmith
   - **Display Name:** John Smith
  
<p align="center">
  <img width="682" height="390" alt="image" src="https://github.com/user-attachments/assets/69a5e5bc-dfc6-4c32-a5e5-12f066fe73e9" />
</p>

4. Open the **Properties** tab then enter the following information:
   - **First Name:** John
   - **Last Name:** Smith
   - **Job Title:** IT Support Specialist
   - **Department:** IT
  
<p align="center">
  <img width="838" height="349" alt="image" src="https://github.com/user-attachments/assets/5342a5eb-bc76-4180-b28b-b5f887a7cc1f" />
</p>

5. Press **Review + Create** then **Create**

<p align="center">
  <img width="1436" height="261" alt="image" src="https://github.com/user-attachments/assets/4697883b-bd44-4152-a48c-443e275fd952" />
</p>

---

### 5) Bulk User Creation

Bulk user creation via CSV import demonstrates how identities are provisioned at scale in a real organization, rather than one at a time. This method is commonly used during onboarding waves, mergers, or initial tenant population.

1. In the **Entra ID** dropdown select **Users** then **All Users**
2. Open the **Bulk Operations** then **Bulk Create (Preview)**
3. Where it says **Upload Your CSV File** upload the **[CreateUsersTemplate](https://github.com/RyanKennon/Entra-Tenet-Setup/blob/main/CreateUsersTemplate.csv)** then **Submit**

<p align="center">
  <img width="854" height="490" alt="image" src="https://github.com/user-attachments/assets/fd7462aa-0ef3-4a07-82ae-101f707d8435" />
</p>

---

### 6) Security Group Creation

Security groups are used to organize users by department and control access to resources and policies. Creating department-based security groups establishes the access structure that later labs in this series will build on for role-based access control and Conditional Access targeting.

1. In the **Entra ID** dropdown select **Groups** then **All Groups** then **+ New Group**
2. Create a **Group** with the following information then press **Create:**
   - **Group Type:** Security
   - **Group Name:** SG-IT-Staff
  
<p align="center">
  <img width="689" height="346" alt="image" src="https://github.com/user-attachments/assets/98d44a1d-2b14-479f-878f-295f9183e689" />
</p>

3. Create **Security Groups** for the **Human Resources, Sales, Finance, Marketing** departments

<p align="center">
  <img width="1167" height="291" alt="image" src="https://github.com/user-attachments/assets/75a1d140-1705-4e99-958e-c372b2504c03" />
</p>

---

### 7) Microsoft 365 Group Creation

Microsoft 365 groups provide collaboration-focused resources such as a shared mailbox, calendar, and Teams workspace. Creating a company-wide Microsoft 365 group demonstrates the distinction between access-control-focused security groups and collaboration-focused Microsoft 365 groups.

1. In the **Entra ID** dropdown select **Groups** then **All Groups** then **+ New Group**
2. Create a **Group** with the following information then press **Create:**
   - **Group Type:** Microsoft 365
   - **Group Name:** M365-AllStaff
   - **Members:** All members
  
<p align="center">
  <img width="733" height="644" alt="image" src="https://github.com/user-attachments/assets/48430114-9389-440b-80d9-360ea1f32f69" />
</p>

---

> **Note:** This lab is intentionally left open. The Entra ID tenant configured 
> here serves as the foundation for all subsequent Entra ID labs in the 
> Entra ID Lab Series.

---

<p align="right">
  <a href="https://github.com/RyanKennon/Entra-ID-Lab-Series-Lab-2-Repo-Name">Lab 2 — Users, Groups & RBAC ➡</a>
</p>
