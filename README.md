# Web Server Hosting Static Website Using AWS CloudFormation

This project demonstrates how to deploy a web server that hosts a static website using AWS services like EC2, S3, and CloudFormation. It includes infrastructure automation, IAM role configuration, and serving content via Apache.

---

## **Overview**
This project automates the deployment of:
1. An **EC2 instance** running Apache as a web server.
2. An **S3 bucket** to store static files (like `index.html`).
3. IAM roles and policies to allow secure access between EC2 and S3.

The static website is hosted on the EC2 instance, with content sourced from the S3 bucket. Explore the web server [here](http://ec2-44-211-127-127.compute-1.amazonaws.com)

---

## **Architecture**

### **Components:**
1. **Amazon EC2**:
   - Hosts the Apache web server to serve the static website.
2. **Amazon S3**:
   - Stores the static HTML file (`index.html`).
3. **IAM Role**:
   - Grants EC2 permissions to access the S3 bucket.
4. **Security Group**:
   - Allows HTTP (port 80) and SSH (port 22) traffic to the EC2 instance.

Here is the architecture diagram generated from `Infrastructure Composer` in `AWS CloudFormation`.
![Architecture Diagram](/architecture.png)

---

## **Setup Instruction**

### **Step 1: Create CloudFormation template file**
1. Use the `cfn-web-server.yaml` provided in this repository.
2. Replace the `ImageId` with a valid Amazon Linux 2 AMI ID for your region.
3. Replace with a unique bucket name.
   
### **Step 2: Deploy the CloudFormation Stack**
1. Open the AWS Management Console → **CloudFormation** → **Create Stack**.
2. Upload the `cfn-web-server.yaml` file.
3. Follow the on-screen instructions to create the stack.
4. Wait for the stack to complete.
5. Note the **S3 bucket name** and **EC2 public DNS** from the Outputs section.

### **Step 3: Upload Your HTML File to S3**
1. Modify `index.html` or use the example provided.
2. Upload `index.html` to the S3 bucket.

### **Step 4: Test Your Web Server**
1. Open the EC2 public DNS in your browser.
2. Verify that the web server runs the static website is displayed.

---

### **Website Output**
   ![Website Output Screenshot](/website.png)

---

## Connect with me 

**Kanika Mathur**  
- [E-mail](mkanika.90@gmail.com)
- [GitHub](https://github.com/KanikaGenesis)  
- [LinkedIn](https://www.linkedin.com/in/kanika-mathur-083080121)  


