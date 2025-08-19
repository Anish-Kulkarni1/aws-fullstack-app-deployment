# Full-Stack Application Deployment on AWS

This project is a demonstration of a complete, cloud-native application deployment using core Amazon Web Services. The goal was to build and deploy a simple To-Do list REST API from scratch, showcasing foundational skills in cloud architecture, networking, and security.

---

### How to Test the API

Directly accessing the endpoint in a web browser can be unreliable due to browser security policies. The recommended way to test this API is by using a dedicated API client like **Postman**.


#### **1. Get All To-Dos (`GET` Request)**
* **Method:** `GET`
* **URL:** `http://51.20.119.193:3000/todos`
* **Result:** You will receive a `200 OK` status and a JSON array of all to-do items (which will be `[]` initially).

#### **2. Create a New To-Do (`POST` Request)**
* **Method:** `POST`
* **URL:** `http://51.20.119.193:3000/todos`
* Go to the **Body** tab, select **raw**, and choose **JSON** from the dropdown.
* Paste the following into the body:
    ```json
    {
        "description": "My first to-do item"
    }
    ```
* **Result:** You will receive a `200 OK` status and the newly created to-do object in the response.

---

### Technologies Used
* **Backend:** Node.js, Express.js
* **Database:** PostgreSQL
* **Cloud Provider:** Amazon Web Services (AWS)

---

### AWS Architecture

This project utilizes a fundamental and robust cloud architecture:

* **Compute:** An **Amazon EC2** instance (`t3.micro`) was provisioned to host the Node.js application server.
* **Database:** An **Amazon RDS** instance was used to create a managed PostgreSQL database, separating the data layer from the compute layer for better scalability and security.
* **Networking & Security:**
    * An **Amazon VPC** provides an isolated network environment for the resources.
    * **Security Groups** were configured to act as a virtual firewall, allowing traffic only on necessary ports (80 for web, 22 for SSH, and 3000 for the application).
    * **Network ACLs** were verified to ensure they allowed all traffic at the subnet level.
