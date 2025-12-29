Perfect choice 👍
I’ll now **convert MOYA into a clickable Figma prototype flow** — in a way that you (or any designer) can **rebuild exactly in Figma** and demo to **investors, partners, or users**.

> ⚠️ Important note (transparent):
> I cannot directly create or share a live Figma link from here, **but** I will give you a **100% Figma-ready blueprint**:
> ✔ Frame sizes
> ✔ Click interactions
> ✔ Navigation logic
> ✔ Prototype connections
> ✔ Naming conventions

If you follow this, the prototype will behave like a **real app**.

---

# 🎯 MOYA – CLICKABLE FIGMA PROTOTYPE FLOW

## 0️⃣ FIGMA FILE SETUP (DO THIS FIRST)

### File Name

**MOYA – Clickable Prototype (MVP)**

### Pages (Exact)

1. `01 – Components`
2. `02 – Customer App`
3. `03 – Provider App`
4. `04 – Admin (Optional)`

---

## 1️⃣ FRAME SETTINGS (IMPORTANT)

### Mobile (Android)

* Width: **360 px**
* Height: **800 px**
* Layout grid: 8px system

### Desktop (Admin)

* Width: **1440 px**

---

# 🟦 PART A: CUSTOMER APP – CLICKABLE FLOW

## FLOW OVERVIEW

```
Splash → Login → OTP → Location →
Home → Category → Request →
Matching → Assigned →
Tracking → Rating → Home
```

---

## SCREEN 1: Splash Screen

**Frame name:** `C01_Splash`

### Interaction

* Prototype:

  * `On After Delay (800ms)`
  * → Navigate to `C02_Login`

---

## SCREEN 2: Login

**Frame:** `C02_Login`

### Clicks

* **Send OTP button**

  * `On Tap → Navigate to C03_OTP`

---

## SCREEN 3: OTP

**Frame:** `C03_OTP`

### Clicks

* **Verify button**

  * `On Tap → Navigate to C04_Location`

---

## SCREEN 4: Location Permission

**Frame:** `C04_Location`

### Clicks

* **Allow Location**

  * `On Tap → Navigate to C05_Home`
* **Set Manually**

  * `On Tap → Navigate to C05_Home`

---

## SCREEN 5: Home

**Frame:** `C05_Home`

### Clicks

* **Service Card (Plumbing, Electrical, etc.)**

  * `On Tap → Navigate to C06_Category`
* **Popular Service**

  * `On Tap → Navigate to C06_Category`

---

## SCREEN 6: Service Category

**Frame:** `C06_Category`

### Clicks

* **Select button**

  * `On Tap → Navigate to C07_RequestForm`

---

## SCREEN 7: Service Request Form

**Frame:** `C07_RequestForm`

### Clicks

* **Submit Request**

  * `On Tap → Navigate to C08_Matching`

---

## SCREEN 8: Matching

**Frame:** `C08_Matching`

### Interaction

* `After Delay (1.5s)`
* → Navigate to `C09_Assigned`

---

## SCREEN 9: Provider Assigned

**Frame:** `C09_Assigned`

### Clicks

* **Call Provider** → No navigation (demo only)
* **Continue**

  * `On Tap → Navigate to C10_Tracking`

---

## SCREEN 10: Job Tracking

**Frame:** `C10_Tracking`

### Clicks

* **Mark Completed (demo button)**

  * `On Tap → Navigate to C11_Rating`

---

## SCREEN 11: Rating

**Frame:** `C11_Rating`

### Clicks

* **Submit Rating**

  * `On Tap → Navigate to C05_Home`

---

# 🟩 PART B: PROVIDER APP – CLICKABLE FLOW

## FLOW OVERVIEW

```
Login → Profile Setup →
Waiting Approval →
Home → Job Request →
Job Details → Complete →
Home
```

---

## SCREEN 1: Provider Login

**Frame:** `P01_Login`

### Click

* **Login**

  * → `P02_ProfileSetup`

---

## SCREEN 2: Profile Setup

**Frame:** `P02_ProfileSetup`

### Click

* **Submit for Approval**

  * → `P03_WaitingApproval`

---

## SCREEN 3: Waiting Approval

**Frame:** `P03_WaitingApproval`

### Interaction

* `After Delay (1.5s)`
* → `P04_Home`

---

## SCREEN 4: Provider Home

**Frame:** `P04_Home`

### Click

* **New Job Card**

  * → `P05_JobRequest`

---

## SCREEN 5: Job Request

**Frame:** `P05_JobRequest`

### Clicks

* **Accept**

  * → `P06_JobDetail`
* **Reject**

  * → Back to `P04_Home`

---

## SCREEN 6: Job Detail

**Frame:** `P06_JobDetail`

### Click

* **Mark Completed**

  * → `P04_Home`

---

# 🧩 COMPONENT INTERACTIONS (REUSABLE)

### Buttons

* Hover → darker shade
* Disabled → gray

### Cards

* On tap → Navigate
* Use `Smart Animate`

### Loaders

* Use simple rotating circle
* Simulate delay transitions

---

# 🎥 HOW TO PRESENT THIS PROTOTYPE

### For Investors

* Show **Customer flow only**
* Emphasize:

  * Simplicity
  * Trust
  * Speed

### For Developers

* Walk through **frame names**
* Explain **navigation logic**

---

# 🏁 FINAL RESULT YOU’LL HAVE

After building this in Figma, you will have:
✅ A clickable MOYA app
✅ Demo-ready prototype
✅ Investor-friendly UX
✅ Developer-clear flows

This is **exactly how early-stage startups pitch**.

---

## 🚀 NEXT (Very Powerful Options)

If you want, I can:
1️⃣ Create **exact Figma component specs (colors, fonts)**
2️⃣ Create **user journey animations**
3️⃣ Convert prototype into **developer tickets (Jira)**
4️⃣ Align each screen with **API endpoints**

Tell me the next number — MOYA is now at **product-demo level** 🚀
