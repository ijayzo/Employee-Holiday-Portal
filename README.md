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

# Usage of Employee Holiday Portal App

Run com.example.demo.EmployeeTravelPackageApplication as a Java Application.

Runs on port of Spring Boot - 8080

API usage

- http://localhost:8080/employee/createEmployee

```JSon
{
	"firstName": "new",
	"lastName": "employee",
	"email": "approved",
	"username": "new.Emp",
	"password": "p@55w0rd",
	"role": "EMPLOYEE"
}
```

- http://localhost:8080/employee/getAllEmployees

```text
Gets All Employees in the Database in JSON format.
```

- http://localhost:8080/employee/deleteEmployee

```text
Front End will use this controller to call for the deleteEmployee service.
```

- http://localhost:8080/flights/getAllFlights
```text
Gets All Flights in the Database in JSON format.
```
- http://localhost:8080/flights/getDirectFromAPI/from/{from}/to/{to}
```text
Gets All Flights from 3rd Party API in JSON format.
{from} and {to} uses three-letter Airport codes. 
```
- http://localhost:8080/flights/getFlights/from/{from}/to/{to}
```text
Gets Specific Flights from 3rd Party API in JSON format.
{from} and {to} uses three-letter Airport codes. 
```
- http://localhost:8080/flights/getOneFlight/{flightID}
```text
Gets a Specific Flight from 3rd Party API in JSon format using a flight ID.
```
- http://localhost:8080/flights/deleteFlights/from/{from}/to/{to}
```text
Deletes Specific Flights (more so used in Front End).
{from} and {to} uses three-letter Airport codes. 
```
- http://localhost:8080/hotel/get
```text
Controller gets used in Front End to Get Hotels fromt the Database in JSon format by Hotel Partner ID.
```
- http://localhost:8080/hotel/all
```text
Gets All Hotels in the Database in JSON format.
```
- http://localhost:8080/hotel/new
```text
Post Controller to create a Hotel in the Database in JSon format.
{
	"hotelLocation": "new",
	"hotelName": "hotel"
}
```
- http://localhost:8080/hotel/delete
```text
Deletes Specific Hotel (more so used in Front End).
```
- http://localhost:8080/auth/login
```
Login Controller, uses JSON format 
{
	"username": "someusernme",
	"password": "password"
}
```
- http://localhost:8080/package/getAllPackages
```text
Gets All Packages in the Database in JSon format.
```
- http://localhost:8080/package/createPackages
```JSON
{
	"employeeId": "6",
	"packageCategory": "STAYCATION",
	"travelDate": "2022-05-02",
	"travelDestination": "Miami",
	"packageDays": "7",
	"packageStatus": "PUBLISHED",
	"packageCost": "8000",
	"hotelPartnerId" : "65",
	"flightId" : "1567",
	"packageDescription": "Beach",
	"totalPackageSignUp": "5"
}
```
- http://localhost:8080/package/updatePackages
```text
Save Controller (above) is used to update the Packages.
```
- http://localhost:8080/package/getOnePackage/{packageID}
```text
Gets a Specific Package by Package ID in JSON format.
```
- http://localhost:8080/package/deletePackage/{packageID}
```text
Deletes a specific Package by Package ID.
Used more so in the Front End.
```

usage is the same as what i did for app3.  just include a readme file with all the controller calls and the expected responses

# Usage of Create React App

This project was bootstrapped with [Create React App](https://github.com/facebook/create-react-app).

## Available Scripts

In the project directory, you can run:

### `npm start`

Runs the app in the development mode.\
Open [http://localhost:3000](http://localhost:3000) to view it in your browser.

The page will reload when you make changes.\
You may also see any lint errors in the console.


# Usage of app3 mailsender

Run com.example.demo.DemoApplication as a Java Application.

Runs on port of Spring Boot - 8070

API usage

- http://localhost:8070/mailapi/sendTestEmail

```txt
Test Email sent successfully
```

- http://localhost:8070/mailapi/sendCancelEmail
- JSON Body: {
  "emailTo": "isaias.jasso@revature.net",
  "cancelReason": "unforseen issues with the supplier",
  "packageDesc": "Super Awesome Miami Beach Package"
  }

```txt
Email sent successfully to isaias.jasso@revature.net
```
monitoring API
- http://localhost:8070/actuator/health

```JSON
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
