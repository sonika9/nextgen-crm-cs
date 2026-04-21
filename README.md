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

This design highlights a clean service-oriented architecture where asynchronous processing and caching are used to optimize performance.

<h3>Application Overview</h3>
<p>Implementation of a CRM module for lead management. This module includes lead scoring predictions based on Machine Learning algorithms.</p>
<h4>This application includes:</h4>
<ul>
  <li>A form where a user can apply to see if its qualified to get a free programming course.</li>
  <li>Backend system to process the information and to show the lead insights by presenting reports and graphs.</li>
  <li>An ML service to calculate the lead scoring predictions.</li>
</ul>
<h4>Use case</h4>
<p>A user fills an application (Free Programming Courses) via a landing page. The data is submited to the Laravel backend system. The system saves the lead data in the database and 
send the lead data to the lead scoring queue to calculate the lead score using the ML service. When the lead scoring is calculated it will be showed in the system Lead reports.</p>
<h3>Technical Implementation & Design Decisions</h3>
<h4>ML Service</h4>
<ul>
  <li>
    ML algorithm: RandomForestClassifier, features analyzed: age, income, years of experience
  </li>
  <li>
    Dataset: The dataset used to generate the model is a generated dataset built for the case study purposes. The dataset columns are:
    age, job, income, years of experience, and a column that indicates if this user has bought a programming course in the past.
  </li>
  <li>
    Python, Flask, Pandas
  </li>
  <li>
    AWS: S3
  </li>
</ul>
<h4>Backend System</h4>
<ul>
  <li>
    Laravel + Blade templates + Tailwindcss
  </li>
  <li>
    AWS: RDS, SQS, Valkey(Redis compatible)
  </li>
  <li>
    CI/CD: Docker, Github Actions
  </li>
</ul>
