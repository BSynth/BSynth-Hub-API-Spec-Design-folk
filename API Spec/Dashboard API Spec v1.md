# 📘 BSynth Hub Dashboard API Spec

This document describes the API structure and sample data format for the BSynth Hub Dashboard Project. 

The backend team can use this as a reference for building the endpoints.

---

## 🧩 API Endpoints

### 1. `GET /projects`
Returns the details of a project including its members.

#### 🔹 Response Example:
```json
{
  "id": 1,
  "project_name": "BSynth Hub",
  "description": "First Project Community Dashboard",
  "start_date": "2025-04-24",
  "end_date": null,
  "status": "in-progress",
  "member_count": 2,
  "members": [
    {
      "nickname": "Boss",
      "fullname": "Sahasawat Rueankaew",
      "role": "Frontend Developer"
    },
    {
      "nickname": "Example",
      "fullname": "Example Dev",
      "role": "Backend Developer"
    }
  ]
}
```

---

### 2. `GET /users`
Returns user profile data.

#### 🔹 Response Example:
```json
{
  "id": 1,
  "nickname": "Boss",
  "fullname": "Sahasawat Rueankaew",
  "age": 25,
  "register_date": "2025-04-24",
  "member_no": 1
}
```

---

## 🛠 Notes for Backend Dev
- Please use ISO 8601 format for all dates.
- `end_date` can be `null` if ongoing.
- `status` can be one of: `planned`, `in-progress`, `completed`.
- Optional: Create additional endpoints like `POST /projects`, `POST /users`, etc. later.

Let me know if you need mock data or frontend integration tips!
