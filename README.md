# Full-Stack Application Deployment on AWS

This project is a demonstration of a complete, cloud-native application deployment using core Amazon Web Services. The goal was to build and deploy a simple To-Do list API from scratch, showcasing foundational skills in cloud architecture, networking, and security.

### Live Demo Endpoint
The backend API is live and can be accessed here:
**[http://51.20.119.193:3000/todos](http://51.20.119.193:3000/todos)**

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
    * **Network ACLs** were verified to ensure they allowed traffic at the subnet level.



---

### Challenges & Learning
Deploying this application involved overcoming real-world networking challenges, such as troubleshooting connection timeouts by systematically debugging security groups, on-server firewalls, and network ACLs. This process provided critical hands-on experience in cloud network diagnostics.
