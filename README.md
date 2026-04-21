<h2>System Design Case Study: Web Application with AWS Infrastructure and ML Module</h2>

<p>This project explores the architecture of a web application that includes a CRM module designed to enhance lead management through data-driven insights. The system incorporates a lead scoring capability that predicts conversion probability using a machine learning model exposed via a decoupled ML service.</p>

The system is deployed on a cloud-based AWS infrastructure and emphasizes scalability, reliability, and separation of concerns. It is built using the following technologies:

* Laravel (core web application / CRM backend)
* Python (Machine Learning service for lead scoring)
* MySQL on Amazon RDS (relational data storage)
* Amazon ECS (container orchestration for services)
* Application Load Balancer (traffic distribution and routing)
* Amazon SQS (asynchronous processing and decoupled communication)
* Valkey (Redis-compatible caching layer for performance optimization)
* Docker (containerization of services)
* GitHub Actions (CI/CD pipeline for automated testing and deployment)

<img width="944" height="624" alt="image" src="https://github.com/user-attachments/assets/e6a996ef-4695-48a4-8bc8-8ee709939aed" />
