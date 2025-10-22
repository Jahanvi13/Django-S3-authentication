#  Django + AWS S3 Authentication & File Upload

A full-stack **Django** project demonstrating secure **user authentication** and **AWS S3 file storage**.  
Users can register, log in, and upload files that are safely stored in an AWS S3 bucket.  
Includes a lightweight dashboard for **graphical representation of uploaded data**.

---

## Features

###  User Authentication
- Register with username, email, and password  
- Secure login/logout using Django’s built-in auth system  
- Password hashing & validation for data safety  

###  AWS S3 Integration
- File uploads directly to AWS S3 using `boto3`  
- Secure environment variable setup (`.env`) for AWS credentials  
- Easy to switch between local and production environments  

###  Data Visualization
- Graphical view of user uploads and file statistics  
- Can be implemented using **Matplotlib** or **Chart.js**

###  Clean Project Structure
- Modular Django apps for authentication, uploads, and visualization  
- Follows best practices for scalability and maintainability  

---

##  Tech Stack

| Layer | Technologies |
| :----- | :------------ |
| **Backend** | Django • Django REST Framework |
| **Cloud** | AWS S3 • boto3 • IAM Roles |
| **Database** | SQLite (local) / PostgreSQL (production) |
| **Visualization** | Matplotlib • Chart.js |
| **Tools** | Git • Python venv • dotenv • GitHub Actions (CI/CD) |

---

## Setup Guide

```bash
# 1️⃣ Clone the repository
git clone https://github.com/Jahanvi13/Django-S3-authentication.git
cd Django-S3-authentication

# 2️⃣ Create and activate a virtual environment
python -m venv .venv
source .venv/bin/activate        # On Windows: .venv\Scripts\activate

# 3️⃣ Install dependencies
pip install -r requirements.txt

# 4️⃣ Create a .env file and configure environment variables
# (You can copy from .env.example if present)
DJANGO_SECRET_KEY=your-secret-key
DEBUG=True
AWS_ACCESS_KEY_ID=your-access-key
AWS_SECRET_ACCESS_KEY=your-secret
AWS_STORAGE_BUCKET_NAME=your-bucket
AWS_REGION=us-east-1

# 5️⃣ Run migrations and start the server
python manage.py migrate
python manage.py runserver

# 6️⃣ Open your browser
# Visit: http://127.0.0.1:8000
