# Employee-Holiday-Portal
Project 2, Team 4, DevOps/SRE 
The Employee Holiday Portal is a web based software that helps organizations offer affordable travel packages to their employees.

# Technologies Used
- BACKEND (App 1 & 3)
•  Java
• Spring Boot
• CloudSQL Postgre
• Gmail SMTP
• Flightscanner API

- FRONTEND (APP2)
• React
• Bootstrap

- TOOLS AND PLATFORMS
• Jenkins
• Docker / Docker HUB
• Google Kubernetes Engine
• Google Cloud Platform
• GITHUB
• Helm
• Prometheus / Grafana
• Promtail / Loki

# Features
• Admin users can create and manage vacation packages.
• Employees can select the best holiday experience for their needs by browsing through the available packages.
• With time saving features like automated alert emails and the ability to download data from popular vacation related 3rd party providers (API).
• Front end allows user to login (Employee/Admin).
• Create and Display Employees/Packages/Hotel Partners.
• Book and Cancel packages.
• Monitoring using Promtail/Prometheus/Loki/Grafana stack.
• Deploying to Kubernetes with Jenkins pipeline with Github Integration.

# To-do list:
• Monitoring Alerts (Email)
• Message Queueing Service
• Reviews and Comments
• SonarQube integration
• Hotel API
• SMS Sending capability
• Discord / Slack Integration
• Add support for Sports and Wellness Events
• Revamped Front End
• Single Sign On
• Add Images to Packages and Content
• Mobile App
• Admin Workflow for Review and
• Approval
• Add Images to Review and Comments

# Getting Started
• git clone https://github.com/ijayzo/Proj2Team4.git
• git clone https://github.com/ijayzo/app3mailsender.git
• git clone https://github.com/ijayzo/React.git 
(include all environment setup steps)
• Only works on GCP
All the code required to get started
Images of what it should look like

# app3 mailsender Usage

Run com.example.demo.DemoApplication as a Java Application.

Runs on port of Spring Boot - 8070

API usage

- http://localhost:8070/mailapi/sendTestEmail

```txt
Test Email sent successfully
```

- http://localhost:8070/mailapi/sendCancelEmail
- JSON Body: {
  "emailTo": "noel.gopez@revature.net",
  "cancelReason": "unforseen issues with the supplier",
  "packageDesc": "Super Awesome Miami Beach Package"
  }

```txt
Email sent successfully to noel.gopez@revature.net
```
monitoring API
- http://localhost:8070/actuator/health

```json
{"status":"UP"}
```

- http://localhost:8070/actuator/prometheus
```properties
# HELP jvm_memory_max_bytes The maximum amount of memory in bytes that can be used for memory management
# TYPE jvm_memory_max_bytes gauge
jvm_memory_max_bytes{area="nonheap",id="CodeHeap 'profiled nmethods'",} 1.2288E8
jvm_memory_max_bytes{area="heap",id="G1 Survivor Space",} -1.0
jvm_memory_max_bytes{area="heap",id="G1 Old Gen",} 3.185573888E9
jvm_memory_max_bytes{area="nonheap",id="Metaspace",} -1.0
jvm_memory_max_bytes{area="nonheap",id="CodeHeap 'non-nmethods'",} 5898240.0
jvm_memory_max_bytes{area="heap",id="G1 Eden Space",} -1.0
```
(Here, you instruct other people on how to use your project after they’ve installed it. This would also be a good place to include screenshots of your project in action.)

# Contributors
Noel Pogi, Richmond Awuah Adjei, Casey Spencer
