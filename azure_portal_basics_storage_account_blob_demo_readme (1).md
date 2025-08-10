# Azure Portal Basics: My First Resource Group + Storage Account 

I decided to walk through the process of creating a free Azure subscription, setting up a Resource Group and a Storage Account, uploading and editing a blob, and then cleaning everything up so I wouldn’t get charged. Here’s exactly what I did.

---

## 0)  Links I Used

- Create a **Free Azure** subscription: [https://azure.microsoft.com/en-us/free/](https://azure.microsoft.com/en-us/free/)
- (Alternative) Create **Pay‑As‑You‑Go**: [https://azure.microsoft.com/en-us/pricing/purchase-options/pay-as-you-go](https://azure.microsoft.com/en-us/pricing/purchase-options/pay-as-you-go)
- **Azure Portal**: [https://portal.azure.com](https://portal.azure.com)

---

## 1) Creating My Azure Subscription

I went to the Free Azure page, clicked Start free, and signed in with my Microsoft account.
After verifying my identity and payment method (there was a small temporary authorization), I landed inside the Azure Portal. [https://portal.azure.com](https://portal.azure.com).

<img width="1614" height="871" alt="portol" src="https://github.com/user-attachments/assets/3091d8bf-959e-4c73-9c76-a28f679e5a70" />
<img width="1553" height="871" alt="creating container" src="https://github.com/user-attachments/assets/42f35185-fa91-4460-8ec7-40a3ce0b1151" />



---

## 2) Sign in to the Azure Portal

1. Open [https://portal.azure.com](https://portal.azure.com) and sign in.
2. Confirm your **Directory + subscription** in the top bar (click your profile → Switch directory if needed).

---

## 3) Quick Tour: Portal Layout

common areas:

- **Resource groups** (left menu → *Resource groups*)
- **Virtual machines** (left menu → *Virtual machines*)
- **Microsoft Entra ID** (formerly Azure AD) (left menu → *Microsoft Entra ID*)

<img width="1924" height="995" alt="Capture" src="https://github.com/user-attachments/assets/d78be477-e691-489e-a24e-03d18bef6130" />

---

## 4) Create a Resource Group

1. In the left menu, click **Resource groups** → **Create**.
2. Choose your **Subscription**.
3. Enter a **Resource group** name .
4. Pick a **Region** close to you.
5. Click **Review + create** → **Create**.

<img width="1920" height="864" alt="resource groups" src="https://github.com/user-attachments/assets/6a349fbf-c64d-4dfe-a658-6bb748ccff4e" />
<img width="1167" height="865" alt="creating a resource group" src="https://github.com/user-attachments/assets/4d2bbebe-22c5-4156-99b9-549a1aa4d98d" />
<img width="864" height="627" alt="review and create" src="https://github.com/user-attachments/assets/af3ce2b5-2324-4a82-b7cc-a5645247d38b" />




---

## 5) Create a Storage Account in that Resource Group

1. Left menu → **Storage accounts** → **Create**.
2. **Basics** tab:
   - **Subscription:** your subscription
   - **Resource group:** select the one you just made 
   - **Storage account name:** globally unique, lowercase 
   - **Region:** same as your RG if possible
   - **Performance:** Standard
   - **Redundancy:** Locally‑redundant storage (LRS) is fine for this demo
3. Click **Review** → **Create** and wait for deployment to complete.
4. Click **Go to resource** when finished.
<img width="1669" height="845" alt="storage accounts" src="https://github.com/user-attachments/assets/eeb242a8-1eac-4496-9d0c-a5e82bc3f893" />
<img width="1356" height="838" alt="create storage account" src="https://github.com/user-attachments/assets/b2b42c76-9d68-47f2-ac8e-ddf5a41b3091" />
<img width="1186" height="823" alt="create storage account 2" src="https://github.com/user-attachments/assets/fda89e2e-3b93-4504-8c23-de8b53654c66" />
---

## 6) Create a Local Text File

- **Windows:** Right‑click desktop → **New → Text Document** → name it `azure-Lab.txt` → open and type: `Hello` → Save.
<img width="1453" height="755" alt="create file" src="https://github.com/user-attachments/assets/128eb4ab-13ba-4c72-9d25-d5892086688d" />
<img width="971" height="659" alt="saving text file" src="https://github.com/user-attachments/assets/8188c100-5ebd-4758-b806-ee9a5b6fc91c" />

---

## 7) Create a Container and Upload the File

1. In your **Storage account**, under **Data storage**, click **Containers**.
2. Click **+ Container** → name it → **Public access level:** *Private* (default) → **Create**.
3. Click the new container (`labtest`) → **Upload**.
4. Select `azure-Lab.txt` from your desktop → **Upload**.
<img width="1484" height="836" alt="clicking our storage account" src="https://github.com/user-attachments/assets/63ed9259-5d9f-442b-ab77-e6c955909089" />
<img width="1553" height="871" alt="creating container" src="https://github.com/user-attachments/assets/21fe9626-9e0d-4d85-9a45-ca17031054c4" />
<img width="1917" height="779" alt="uploading file" src="https://github.com/user-attachments/assets/f0347d2f-f380-44ad-986c-86db45f2130d" />
<img width="1918" height="763" alt="uploading file2" src="https://github.com/user-attachments/assets/eb2c769d-65e4-4b15-a1fa-87413e3d07e4" />
<img width="1915" height="590" alt="uploaded" src="https://github.com/user-attachments/assets/6ccc91ab-0cc3-42a1-935a-dd1ad573b926" />







---

## 8) Edit the Blob in the Portal

1. Inside the container, click the uploaded `azure-Lab.txt` blob.
2. Click **Edit** (or **Edit (preview)**) in the top bar.
3. Append a new line, e.g., `Edited in Azure Portal.` → click **Save**.
<img width="1920" height="821" alt="click the dots" src="https://github.com/user-attachments/assets/ebaff115-f472-4307-a62e-71b79fcf8e29" />
<img width="1655" height="869" alt="edited file" src="https://github.com/user-attachments/assets/295d19f7-b98b-4480-af9a-66f512a14177" />





---

## 9) Download and Verify

1. With `azure-Lab.txt` selected, click **Download** to save a copy locally 
2. Open the downloaded file and confirm it includes your edit.
<img width="1711" height="795" alt="downloaded file" src="https://github.com/user-attachments/assets/521ea029-1c9b-41f3-97f9-5d2a46aba4d2" />



---

## 10) Clean Up (Delete the Resource Group)

> **Important:** This prevents ongoing charges.

1. Left menu → **Resource groups** → select `rg-azure-basics-demo`.
2. Click **Delete resource group**.
3. Type the RG name to confirm → **Delete**.
4. Wait until status shows **Deleted** (may take a minute or two).

<img width="1539" height="848" alt="delete resource group" src="https://github.com/user-attachments/assets/9f87fe88-bd0e-4428-b645-819ee07d6069" />
<img width="1562" height="868" alt="delete resource group2" src="https://github.com/user-attachments/assets/62a22a07-6096-4209-b04f-4b26ba27fcb2" />
<img width="1798" height="831" alt="deleted group" src="https://github.com/user-attachments/assets/8eced314-43da-4d80-8c36-cfe39b78555f" />




---

## 11) Verify Deletion & Costs

1. Confirm the RG is gone from **Resource groups**.
2. Go to **Cost Management + Billing → Cost Management → Cost analysis**.
3. Set the **Scope** to your subscription and review any costs (should be minimal/zero for this short demo).


---

## 12) Notes & Tips

- **Never forget cleanup:** Delete resource groups when done with demos/labs.
- **Naming:** Use concise, unique names. Lowercase letters and numbers are safest for storage account names.
- **Regions:** Keep resources in the same region to minimize latency and simplify costs.
- **Permissions:** If you’re using a work/school account, your tenant admin might restrict creation of certain resources.

---

