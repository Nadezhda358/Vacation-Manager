# 🏖️ Vacation Manager

**Vacation Manager** is a web-based system built with **ASP.NET Core** for managing employee vacations, teams, roles, and projects within an organization.  
Employees can submit requests for **paid**, **unpaid**, or **sick leave**, which are approved by a **Team Lead** or the **CEO**.

---

## 🚀 Features

### 👤 User Management
- User authentication (username & password)  
- Each user has: first name, last name, role, and team  
- CRUD operations for users (available only to CEO)  
- Filter and search by username, first name, last name, or role  
- Paginated user list (10, 25, or 50 per page)  
- Assign users to teams from the user details view  

### 🧩 Roles
- Roles: `CEO`, `Team Lead`, `Developer`, `Unassigned`  
- Display all roles with number of users assigned  
- CRUD operations (CEO only)  
- View all users belonging to a given role  

### 👨‍💻 Teams
- Each team includes:
  - Team name  
  - Project  
  - Developers  
  - Team leader  
- CRUD operations for teams  
- Filter teams by name or project  
- Add or remove team members from the team details view  

### 📁 Projects
- Each project includes:
  - Name  
  - Description  
  - Teams working on it  
- CRUD operations for projects  
- Filter by project name or description  
- Manage team assignments directly from project details  

### 🗓️ Vacation Requests
- Supported types:
  - Paid leave  
  - Unpaid leave  
  - Sick leave (with medical document attachment)  
- Fields include:
  - Start date / End date  
  - Creation date  
  - Half-day flag (disabled for sick leave)  
  - Approval status  
- Edit or delete requests before approval  
- Team Leads and CEO can approve requests  
- Filter requests by creation date  
- Paginated list of requests  

---

## 🔐 Roles and Permissions

| Role | Permissions |
|------|--------------|
| **CEO** | Full CRUD access (users, roles, teams, projects, vacations) |
| **Team Lead** | Approve vacation requests for their team |
| **Developer** | Create, edit, and delete own vacation requests |
| **Unassigned** | Restricted access until assigned a role |

---

## ✅ Validation Rules
- Empty fields are not allowed  
- Dates must be logical (e.g., “end date” cannot be before “start date”)  
- Text fields have length limits  
- Sick leave requires a valid file upload  

---