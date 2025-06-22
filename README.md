# AWS Glue Crawler Project – Banking Transaction Data Catalog

This project demonstrates how to use **AWS Glue Crawlers** to automatically detect and catalog structured CSV data stored in **Amazon S3**, within a **real-world banking scenario**.

---

## 🎯 Objective

XYZ Bank stores a vast number of customer transactions in CSV format across cloud locations. The goal of this project is to:
- Upload banking transaction data into Amazon S3
- Create an AWS Glue database
- Configure and run a Glue Crawler
- Automatically detect table schemas and catalog the data

---

## 🧰 AWS Services Used

- **Amazon S3** – Cloud object storage for raw banking data
- **AWS IAM** – Permissions and role management
- **AWS Glue (Crawler + Data Catalog)** – Metadata discovery and schema generation

---

## 📁 Project Steps

### 1. Created S3 Bucket and Uploaded Data
- Bucket name: `awsgluudemo2`
- Uploaded: `banking-txn.csv` (sample dataset)

### 2. IAM Role for AWS Glue
- Created role: `awsgluedemo2-role`
- Gave it `AdministratorAccess` (for demo purposes)

### 3. AWS Glue Database
- Created database: `bank`

### 4. Configured AWS Glue Crawler
- Name: `bank-data`
- Source: S3 bucket `awsgluudemo2`
- IAM Role: `awsgluedemo2-role`
- Target Database: `bank`

### 5. Ran the Crawler
- Successfully discovered the schema and added a table to the `bank` database

---

## 📊 Final Table Schema

| Column Name        | Data Type |
|--------------------|-----------|
| customer name      | string    |
| address            | string    |
| amount             | double    |
| transaction date   | string    |
| transaction type   | string    |

---

## 🖼️ Screenshots (Key Steps)

> 📸 Below are the important screenshots showing the end-to-end execution of the project.

1. **Created S3 Bucket**  
   ![Image](https://github.com/user-attachments/assets/078ca787-08fc-403b-9057-6e7a76b7f797)

2. **Uploaded banking-txn.csv to S3**  
   ![Image](https://github.com/user-attachments/assets/86b33b08-37f7-4966-847a-c2dd0ae9557c)

3. **Navigated to IAM Console**  
   ![Image](https://github.com/user-attachments/assets/f8fa439c-6b11-4e34-a6e6-95125a180bbb)

4. **Created IAM Role for AWS Glue**  
   ![Image](https://github.com/user-attachments/assets/e8036029-1ea9-4ca9-a486-b43bfe9341bb)

5. **Attached AdministratorAccess**  
   ![image](https://github.com/user-attachments/assets/4ac1557c-0649-445c-88f2-d1686684f756)

6. **Confirmed Role Created (glue-gp)**  
   ![image](https://github.com/user-attachments/assets/14042f9f-98e5-4628-8e24-e153b9af1510)

7. **Opened Glue Console**  
   ![Image](https://github.com/user-attachments/assets/2d9e4ef9-102a-46a0-b33e-c8fcecf2f325)

8. **Created Glue Database - bank**  
   ![Image](https://github.com/user-attachments/assets/e966ede5-9224-4563-be1f-ef09fda1c0e2)

9. **Started Crawler Setup - bank-data**  
   ![Image](https://github.com/user-attachments/assets/d9e65417-dc15-4533-bd7e-fbee8cac4e84)

10. **Selected S3 as Data Source**  
    ![Image](https://github.com/user-attachments/assets/4d271eac-f49e-4aa1-84e0-513dba57a9b0)

11. **Browsed and Chose awsgluudemo2**  
     ![Image](https://github.com/user-attachments/assets/94e45d79-5597-4ca8-ac26-27da7040ebfe)

12. **Selected IAM Role awsgluedemo2-role for the crawler**  
    ![Image](https://github.com/user-attachments/assets/b74be033-8ee6-407b-bfe5-2f1430423641)

13. **Set Target Database as bank**  
    ![Image](https://github.com/user-attachments/assets/e3278dee-52b8-4997-ba9c-c377931d151f)

14. **Created the Crawler**  
    ![Image](https://github.com/user-attachments/assets/b24fb50d-b0e8-458c-ad69-106d4a7a9695)

15. **Ran the Crawler**  
    ![Image](https://github.com/user-attachments/assets/bc97f701-61e6-4615-9c6c-787de3e0f4ce)

16. **Crawler Status: Completed**  
    ![Image](https://github.com/user-attachments/assets/a9be210a-dca2-40ae-99e7-8817f3e4a311)

17. **Viewed Database**  
    ![Image](https://github.com/user-attachments/assets/9a6af804-7f75-405d-8a81-de22e653da30)

18. **Final Schema Output in Data Catalog**  
    ![Image](https://github.com/user-attachments/assets/5e1557e6-fa5d-4b7f-a164-b5d5a62cd919)

---

## 📄 License

This project is licensed under the [MIT License](LICENSE).

---
