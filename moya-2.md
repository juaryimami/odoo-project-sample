Perfect.
Below is a **developer-ready, implementation-level App Feature Specification** for **MOYA**, written exactly how you would give it to developers (or use yourself, since you already work with Odoo & backend systems).

This is **not marketing** — this is **build documentation**.

---

# 📱 MOYA – APP FEATURE SPECIFICATION (DEVELOPER-READY)

## 1. SYSTEM OVERVIEW

**Platform Type:** On-demand service marketplace
**Region:** Addis Ababa, Ethiopia
**Primary Platforms:**

* Android (Customer App)
* Android (Service Provider App)
* Web Admin Dashboard

**Architecture (Recommended)**

* Mobile: Flutter (single codebase) OR Native Android
* Backend: Odoo (Community) OR Django/Node
* Database: PostgreSQL
* Maps: Google Maps / OpenStreetMap
* Auth: Phone number + OTP
* Payments (Phase 2): Telebirr

---

## 2. USER ROLES

### 2.1 Customer

* Requests services
* Tracks providers
* Rates service

### 2.2 Service Provider

* Accepts jobs
* Manages availability
* Gets rated

### 2.3 Admin

* Verifies providers
* Manages services
* Controls disputes
* Manual job assignment

---

## 3. CUSTOMER APP – FEATURES

### 3.1 Authentication

**Required**

* Phone number login
* OTP verification
* Profile creation (name, location)

**Optional (Later)**

* Email
* Profile photo

---

### 3.2 Home Screen

**Components**

* Service categories (grid)
* “Request Service” CTA
* Popular services
* Location selector

**Data**

* Services (id, name, icon)
* Location (lat, lng)

---

### 3.3 Service Request Flow

1. Select service category
2. Enter details (description, images optional)
3. Select location
4. Confirm request

**Backend**

```json
{
  "customer_id": 12,
  "service_id": 3,
  "description": "Leaking pipe",
  "location": { "lat": 9.03, "lng": 38.74 }
}
```

---

### 3.4 Provider Matching

**Phase 1 (Manual + Auto Hybrid)**

* System suggests providers
* Admin can override

**Phase 2**

* Auto-match based on:

  * Distance
  * Availability
  * Rating

---

### 3.5 Job Tracking

* Status: Requested → Assigned → In Progress → Completed
* Provider info shown
* Call provider (masked number)

---

### 3.6 Ratings & Reviews

* 1–5 stars
* Optional comment
* Mandatory after job completion

---

## 4. SERVICE PROVIDER APP – FEATURES

### 4.1 Authentication

* Phone number login
* OTP verification

---

### 4.2 Profile Setup (CRITICAL)

**Required**

* Full name
* Service category
* Area of operation
* National ID upload
* Profile photo

**Admin Approval Required**

---

### 4.3 Job Requests

* Real-time job notifications
* Accept / Reject
* Timeout logic

---

### 4.4 Job Management

* Start job
* Mark completed
* Add job notes

---

### 4.5 Earnings Dashboard

* Completed jobs
* Daily / weekly summary
* Commission breakdown (Phase 2)

---

### 4.6 Availability Toggle

* Online / Offline
* Working hours

---

## 5. ADMIN DASHBOARD (WEB)

### 5.1 User Management

* Customers list
* Providers list
* Block / suspend

---

### 5.2 Provider Verification

* Review documents
* Approve / reject
* Assign service categories

---

### 5.3 Job Management

* View all jobs
* Manually assign provider
* Change job status

---

### 5.4 Service Management

* Add/edit service categories
* Price range suggestion (ETB)

---

### 5.5 Dispute Management

* View complaints
* Resolve manually
* Apply penalties

---

## 6. CORE DATA MODELS (SIMPLIFIED)

### User

```python
id
phone
role (customer/provider/admin)
```

### Provider

```python
user_id
services[]
rating
verified
```

### Service

```python
id
name
base_price_range
```

### Job

```python
id
customer_id
provider_id
service_id
status
location
```

---

## 7. NON-FUNCTIONAL REQUIREMENTS

* Response time < 2 seconds
* Offline handling (basic)
* Secure OTP flow
* Data encryption
* Audit logs (admin)

---

## 8. MVP SCOPE (WHAT TO BUILD FIRST)

### MUST HAVE (Launch)

✅ Phone login
✅ Service request
✅ Provider matching
✅ Admin control
✅ Ratings

### NICE TO HAVE (Later)

⏳ Telebirr
⏳ Chat
⏳ Promotions
⏳ Multi-city

---

## 9. DEVELOPMENT TIMELINE (2-PERSON TEAM)

| Week | Task              |
| ---- | ----------------- |
| 1    | Architecture + DB |
| 2    | Auth & Profiles   |
| 3    | Service flow      |
| 4    | Provider app      |
| 5    | Admin dashboard   |
| 6    | Testing & Pilot   |

---

## 10. DEVELOPER HANDOFF NOTES (IMPORTANT)

* **Manual control early = fewer failures**
* **Trust > automation**
* Keep UI extremely simple
* Addis internet conditions matter

---

## 🧠 Final Advice (Founder Level)

If MOYA works manually with **100 jobs/week**, it will work automatically with **10,000 jobs/month**.

---

## NEXT (Highly Recommended)

I can now:

1. Convert this into a **technical specification PDF**
2. Create **API endpoint documentation**
3. Create **database schema (SQL)**
4. Write **Odoo-based module structure**
5. Design **wireframes (screens)**

Tell me the next number(s).
