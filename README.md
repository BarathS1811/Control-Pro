
# Construction ERP Tool (Django + Streamlit Compatible)

A full-featured ERP system for UAE-based construction companies to manage:

- 👷 Employee records (CRUD)
- 🧰 Asset issuance and replacement tracking
- 🕒 Attendance with project linkage
- 💵 Payroll with PDF payslip generation
- 🧾 Petty cash management with receipts
- 🗂️ Multi-project and multi-role user access

---

## 🔐 User Access Roles

| Role         | Permissions                                                                 |
|--------------|------------------------------------------------------------------------------|
| Proprietor   | Full access to everything                                                   |
| Admin        | Full access except project-user assignment                                  |
| Site Manager | Can manage employees, attendance, and request assets                        |
| Time Keeper  | Can mark attendance and view employee info only                             |

---

## 🚀 Features

- User registration & login
- Role-based dashboard views
- Bootstrap 5 UI with crispy-forms
- PDF/Excel reports (WeasyPrint, django-import-export)
- Clean Django structure
- `Streamlit` integration placeholder (`app.py`)

---

## ⚙️ Installation

```bash
git clone <your-repo>
cd construction_erp_streamlit_django

# Install dependencies
pip install -r requirements.txt

# Run migrations
python manage.py makemigrations
python manage.py migrate

# Run server
python manage.py runserver
```

---

## 🧪 Super Admin Setup

To access Django Admin:

```bash
python manage.py createsuperuser
```

---

## 📄 Streamlit Mode

```bash
streamlit run app.py
```

You can extend `app.py` to interact with Django views or expose APIs.

---

## 🗃️ Directory Structure

```
construction_erp_streamlit_django/
├── app.py                        # Streamlit entry
├── manage.py                    # Django entry
├── requirements.txt
├── users/
│   └── templates/registration/register.html
├── employees/
│   └── templates/employees/
│       ├── employee_list.html
│       ├── employee_form.html
│       └── employee_confirm_delete.html
```

---

## 🛡️ Production Setup (Recommended)

- Use Gunicorn + Nginx
- Use PostgreSQL instead of SQLite
- Use Certbot for HTTPS setup
- Configure Streamlit on subdomain if needed

---

📫 Need help? Contact your developer or raise an issue.
