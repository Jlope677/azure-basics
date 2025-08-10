# Azure Portal Basics: Create a Resource Group + Storage Account 

 This shows how to create a free Azure subscription, sign in to the Azure Portal, create a Resource Group and a Storage Account, upload and edit a text file (blob), then clean up resources and check costs.

---

## 0) Links

- Create a **Free Azure** subscription: [https://azure.microsoft.com/en-us/free/](https://azure.microsoft.com/en-us/free/)
- (Alternative) Create **Pay‑As‑You‑Go**: [https://azure.microsoft.com/en-us/pricing/purchase-options/pay-as-you-go](https://azure.microsoft.com/en-us/pricing/purchase-options/pay-as-you-go)
- **Azure Portal**: [https://portal.azure.com](https://portal.azure.com)

---

## 1) Create a Subscription

1. Go to the Free Azure page and click **Start free**. Sign in with your Microsoft account.
2. Complete the identity and payment verification (a small, temporary authorization may appear).
3. When finished, you’ll land in the **Azure Portal** or you can open it directly at [https://portal.azure.com](https://portal.azure.com).

<img width="1614" height="871" alt="portol" src="https://github.com/user-attachments/assets/3091d8bf-959e-4c73-9c76-a28f679e5a70" />


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
<img width="1484" height="836" alt="clicking our storage account" src="https://github.com/user-attachments/assets/342e91f6-086e-4736-8c3b-32d8cfeed129" />
<img width="1553" height="871" alt="creating container" src="https://github.com/user-attachments/assets/1fd1c885-bf17-4d0c-b598-a1f5ca187a57" />




---

## 6) Create a Local Text File

- **Windows:** Right‑click desktop → **New → Text Document** → name it `hello.txt` → open and type: `Hello from Azure!` → Save.
- **macOS:** Open **TextEdit** → **TextEdit → Settings/Preferences** → set **Format: Plain text** → create `hello.txt`, type `Hello from Azure!` → Save to Desktop.

📸 **Add screenshot:** Local text file open in Notepad/TextEdit

---

## 7) Create a Container and Upload the File

1. In your **Storage account**, under **Data storage**, click **Containers**.
2. Click **+ Container** → name it (e.g., `files`) → **Public access level:** *Private* (default) → **Create**.
3. Click the new container (`files`) → **Upload**.
4. Select `hello.txt` from your desktop → **Upload**.

📸 **Add screenshot:** Container list with `files`\
📸 **Add screenshot:** Upload panel with `hello.txt`

---

## 8) Edit the Blob in the Portal

1. Inside the container, click the uploaded `hello.txt` blob.
2. Click **Edit** (or **Edit (preview)**) in the top bar.
3. Append a new line, e.g., `Edited in Azure Portal.` → click **Save**.

> If *Edit* isn’t available, use **Open → Open in text editor** or download/edit/re‑upload.

📸 **Add screenshot:** Blob editor view with the extra line added

---

## 9) Download and Verify

1. With `hello.txt` selected, click **Download** to save a copy locally (e.g., `hello (1).txt`).
2. Open the downloaded file and confirm it includes your edit.

📸 **Add screenshot:** Local view of the downloaded file showing both lines

---

## 10) Clean Up (Delete the Resource Group)

> **Important:** This prevents ongoing charges.

1. Left menu → **Resource groups** → select `rg-azure-basics-demo`.
2. Click **Delete resource group**.
3. Type the RG name to confirm → **Delete**.
4. Wait until status shows **Deleted** (may take a minute or two).

📸 **Add screenshot:** Delete confirmation dialog\
📸 **Add screenshot:** RG list no longer shows the group

---

## 11) Verify Deletion & Costs

1. Confirm the RG is gone from **Resource groups**.
2. Go to **Cost Management + Billing → Cost Management → Cost analysis**.
3. Set the **Scope** to your subscription and review any costs (should be minimal/zero for this short demo).

📸 **Add screenshot:** Cost analysis chart (zero/near‑zero cost)

---

## 12) Notes & Tips

- **Never forget cleanup:** Delete resource groups when done with demos/labs.
- **Naming:** Use concise, unique names. Lowercase letters and numbers are safest for storage account names.
- **Regions:** Keep resources in the same region to minimize latency and simplify costs.
- **Permissions:** If you’re using a work/school account, your tenant admin might restrict creation of certain resources.

---

## 13) (Optional) GitHub README Template Block

Copy this into your own repo’s `README.md` and replace the `📸` lines with your screenshots.

```markdown
# Azure Portal Basics Demo

- [x] Created subscription  
- [x] Signed in to Azure Portal  
- [x] Created Resource Group  
- [x] Created Storage Account  
- [x] Uploaded & edited a blob  
- [x] Verified changes locally  
- [x] Deleted Resource Group  
- [x] Checked Cost Management

## Screenshots
📸 Subscription created / Portal home
📸 Resource Group creation
📸 Storage Account created
📸 Container + Upload dialog
📸 Blob Edit view
📸 Downloaded file with changes
📸 Cost analysis
```

---

## 14) Troubleshooting

- **Can’t create resources?** Check your subscription/tenant permissions, or verify you’re not in a disabled/free‑trial‑expired state.
- **Storage account name already taken?** Pick a more unique lowercase name (must be 3–24 chars, letters/numbers only).
- **Blob Edit button missing?** Use *Open in text editor* or download → edit → upload a new version.
- **Costs showing up?** Filter Cost Analysis by subscription and time range; ensure the RG is deleted and wait a few minutes.

---

**That’s it!** You created, tested, and cleaned up basic Azure resources—and verified your costs. ✅

