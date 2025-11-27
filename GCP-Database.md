# Deploying and Managing a Database on GCP

## Objective
I set up and managed a relational database on Google Cloud SQL, applied security best practices, and enabled automated backups and scaling.

---

## 1. Create a Cloud SQL Instance
- I navigated to the GCP Console.
- I created a Cloud SQL instance using **MySQL**.
- I selected the appropriate machine type and storage based on project requirements.


### I added Screenshots
![alt text](images/createdMySQL.png)

---

## 2. Configure Security and Access
- I set up IAM roles to control access to the Cloud SQL instance.
### I added Screenshots
![alt text](images/roles1.png)
![alt text](images/roles2.png)

- I enabled SSL/TLS encryption to secure connections.

![alt text](images/SSLenable.png)

- I restricted access using **VPC** and **authorized networks**.


![alt text](images/accessrestrict.png)

---

## 3. Enable Backups and High Availability
- I enabled **automated daily backups**.
- I turned on **point‑in‑time recovery**.

### I added Screenshots
![alt text](images/dailybackup.png)

- I created a **read replica** to improve performance and support scaling.


![alt text](images/replica.png)


---

## 4. Connect to the Database

### ✔ Using Cloud Shell  
I connected to my instance using:

```
gcloud sql connect learning-sql-db --user=root
```

### I added Screenshots
![alt text](images/mysql.png)

---

### ✔ Using MySQL Workbench  
- I Downloaded and installed and opened MySQL Workbench.

### I added Screenshots
![alt text](images/workbenchdownload.png)

- I added a new connection with:
  - Public IP of my instance  
  - Username: root  
  - Password: (the password I created)
- I successfully connected to my Cloud SQL database locally.


### I added Screenshots
![alt text](images/workbench.png)

---

## Completion
I completed all steps of deploying, securing, backing up, scaling, and connecting to my Cloud SQL database as part of this learning project.
