# Azure Portal Basics: My First Resource Group + Storage Account

I decided to walk through the process of creating a free Azure subscription, setting up a Resource Group and a Storage Account, uploading and editing a blob, and then cleaning everything up so I wouldn’t get charged. Here’s exactly what I did.

---

## 0) Links I Used

- Free Azure subscription: [https://azure.microsoft.com/en-us/free/](https://azure.microsoft.com/en-us/free/)  
- Pay-As-You-Go (alternate option): [https://azure.microsoft.com/en-us/pricing/purchase-options/pay-as-you-go](https://azure.microsoft.com/en-us/pricing/purchase-options/pay-as-you-go)  
- Azure Portal: [https://portal.azure.com](https://portal.azure.com)

---

## 1) Creating My Azure Subscription

I went to the Free Azure page, clicked **Start free**, and signed in with my Microsoft account.  
After verifying my identity and payment method (there was a small temporary authorization), I landed inside the **Azure Portal**.

<img width="1614" height="871" alt="portol" src="https://github.com/user-attachments/assets/3091d8bf-959e-4c73-9c76-a28f679e5a70" />
<img width="1553" height="871" alt="creating container" src="https://github.com/user-attachments/assets/42f35185-fa91-4460-8ec7-40a3ce0b1151" />

---

## 2) Signing In to the Azure Portal

I opened [https://portal.azure.com](https://portal.azure.com), signed in, and checked my **Directory + subscription** from the top bar. Everything looked good.

---

## 3) Quick Look Around

I took a moment to explore the layout:  
- **Resource groups**  
- **Virtual machines**  
- **Microsoft Entra ID** (formerly Azure AD)

<img width="1924" height="995" alt="Capture" src="https://github.com/user-attachments/assets/d78be477-e691-489e-a24e-03d18bef6130" />

---

## 4) Creating My Resource Group

I clicked **Resource groups → Create**.  
I selected my subscription, entered a resource group name, picked a region close to me, and clicked **Review + create** → **Create**.  
A few moments later, my new resource group was ready.

<img width="1920" height="864" alt="resource groups" src="https://github.com/user-attachments/assets/6a349fbf-c64d-4dfe-a658-6bb748ccff4e" />
<img width="1167" height="865" alt="creating a resource group" src="https://github.com/user-attachments/assets/4d2bbebe-22c5-4156-99b9-549a1aa4d98d" />
<img width="864" height="627" alt="review and create" src="https://github.com/user-attachments/assets/af3ce2b5-2324-4a82-b7cc-a5645247d38b" />

---

## 5) Creating My Storage Account

Next, I went to **Storage accounts → Create**.  
On the **Basics** tab, I set:
- Subscription: my free Azure subscription  
- Resource group: the one I just created  
- Storage account name: a unique, lowercase name  
- Region: same as my resource group  
- Performance: Standard  
- Redundancy: Locally-redundant storage (LRS)  

I clicked **Review** → **Create** and waited for deployment. Then I opened the resource.

<img width="1669" height="845" alt="storage accounts" src="https://github.com/user-attachments/assets/eeb242a8-1eac-4496-9d0c-a5e82bc3f893" />
<img width="1356" height="838" alt="create storage account" src="https://github.com/user-attachments/assets/b2b42c76-9d68-47f2-ac8e-ddf5a41b3091" />
<img width="1186" height="823" alt="create storage account 2" src="https://github.com/user-attachments/assets/fda89e2e-3b93-4504-8c23-de8b53654c66" />

---

## 6) Making a Local Text File

On my Windows desktop, I created a new text document named `azure-Lab.txt`, typed “Hello” in it, and saved.

<img width="1453" height="755" alt="create file" src="https://github.com/user-attachments/assets/128eb4ab-13ba-4c72-9d25-d5892086688d" />
<img width="971" height="659" alt="saving text file" src="https://github.com/user-attachments/assets/8188c100-5ebd-4758-b806-ee9a5b6fc91c" />

---

## 7) Creating a Container and Uploading My File

Inside my new storage account, I went to **Containers**, clicked **+ Container**, named it, kept **Public access level** set to Private, and created it.  
I opened the container, clicked **Upload**, selected my `azure-Lab.txt` file from the desktop, and uploaded it.

<img width="1484" height="836" alt="clicking our storage account" src="https://github.com/user-attachments/assets/63ed9259-5d9f-442b-ab77-e6c955909089" />
<img width="1553" height="871" alt="creating container" src="https://github.com/user-attachments/assets/21fe9626-9e0d-4d85-9a45-ca17031054c4" />
<img width="1917" height="779" alt="uploading file" src="https://github.com/user-attachments/assets/f0347d2f-f380-44ad-986c-86db45f2130d" />
<img width="1918" height="763" alt="uploading file2" src="https://github.com/user-attachments/assets/eb2c769d-65e4-4b15-a1fa-87413e3d07e4" />
<img width="1915" height="590" alt="uploaded" src="https://github.com/user-attachments/assets/6ccc91ab-0cc3-42a1-935a-dd1ad573b926" />

---

## 8) Editing the Blob in the Portal

From the container, I opened the `azure-Lab.txt` blob and clicked **Edit**.  
I added a new line:  
```
Edited in Azure Portal.
```  
Then I clicked **Save**.

<img width="1920" height="821" alt="click the dots" src="https://github.com/user-attachments/assets/ebaff115-f472-4307-a62e-71b79fcf8e29" />
<img width="1655" height="869" alt="edited file" src="https://github.com/user-attachments/assets/295d19f7-b98b-4480-af9a-66f512a14177" />

---

## 9) Downloading and Checking My Edit

I downloaded the updated blob to my computer and opened it — my new line was there.

<img width="1711" height="795" alt="downloaded file" src="https://github.com/user-attachments/assets/521ea029-1c9b-41f3-97f9-5d2a46aba4d2" />

---

## 10) Cleaning Up

To avoid charges, I deleted everything.  
I went to **Resource groups**, selected mine, clicked **Delete resource group**, typed the name to confirm, and waited until it was gone.

<img width="1539" height="848" alt="delete resource group" src="https://github.com/user-attachments/assets/9f87fe88-bd0e-4428-b645-819ee07d6069" />
<img width="1562" height="868" alt="delete resource group2" src="https://github.com/user-attachments/assets/62a22a07-6096-4209-b04f-4b26ba27fcb2" />
<img width="1798" height="831" alt="deleted group" src="https://github.com/user-attachments/assets/8eced314-43da-4d80-8c36-cfe39b78555f" />

---

## 11) Verifying Deletion & Costs

I checked **Resource groups** to make sure mine was gone, then went to **Cost Management + Billing → Cost analysis**. My costs were at zero.

---

## 12) My Notes & Takeaways

- Always delete your resource groups when you’re done with a lab.  
- Keep names short, lowercase, and unique.  
- Use the same region for all related resources to keep things simple.  
