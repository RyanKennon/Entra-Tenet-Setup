<p align="center">
  <img width="474" height="279" alt="image" src="https://github.com/user-attachments/assets/584155f5-b617-48f1-bd7c-22029abedfb7" />
</p>

# Entra-Tenet-Setup

---

### 1) 

1. In the **Entra ID** dropdown then select **Overview**
2. For the **Name** enter **Kennon Technologies** then **Save**

<p align="center">
  <img width="709" height="373" alt="image" src="https://github.com/user-attachments/assets/e14a37df-084e-4d65-99a8-bc70f29875b2" />
</p>

---

### 2) Company Branding

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

### 5) 

1. In the **Entra ID** dropdown select **Users** then **All Users**
2. Open the **Bulk Operations** then **Bulk Create (Preview)**
3. Where it says **Upload Your CSV File** upload the **[CreateUsersTemplate](https://github.com/RyanKennon/Entra-Tenet-Setup/blob/main/CreateUsersTemplate.csv)** then **Submit**

<p align="center">
  <img width="854" height="490" alt="image" src="https://github.com/user-attachments/assets/fd7462aa-0ef3-4a07-82ae-101f707d8435" />
</p>

---

### 6) Security Group Creation

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

1. In the **Entra ID** dropdown select **Groups** then **All Groups** then **+ New Group**
2. Create a **Group** with the following information then press **Create:**
   - **Group Type:** Microsoft 365
   - **Group Name:** M365-AllStaff
   - **Members:** All members
  
<p align="center">
  <img width="733" height="644" alt="image" src="https://github.com/user-attachments/assets/48430114-9389-440b-80d9-360ea1f32f69" />
</p>

---
