HIT DevOps Exercise - JSP Deployment and Monitoring
Overview
This exercise is designed to provide hands-on experience with continuous integration and deployment (CI/CD) processes using Jenkins, deploying a JavaServer Pages (JSP) application to Tomcat, and monitoring the web application's availability. Participants will gain practical skills in automating build and deployment processes and ensuring the application's reliability.

Contributors:
Dor Slagter
Shahar Tevelov
Objectives
Configure a Jenkins job to automate the deployment of a JSP file.
Deploy the JSP application to a Tomcat server.
Monitor the application to ensure its availability.
Prerequisites
Jenkins server with necessary plugins installed (e.g., Git, Deploy to container).
Tomcat server set up and running.
Basic understanding of Git, Jenkins, and Tomcat.
Steps
1. Prepare Your Environment
Ensure that Jenkins and Tomcat are installed and properly configured on your system or accessible servers.

2. Jenkins Job Configuration
Create a new job in Jenkins: Select New Item, name your job (e.g., JSPDeployment), and choose Freestyle project.

Source Code Management: Configure the job to pull the JSP file from your Git repository by selecting Git and providing the repository URL and credentials if necessary.

Build Triggers: Choose how you want to trigger the build (e.g., periodically, on push to the repository).

Build: Add a build step that compiles your JSP file if necessary. For simple JSP files, this might not be required.

Post-build Actions: Use the Deploy to container Plugin to deploy the JSP file to Tomcat. Configure the Tomcat URL, credentials, and the WAR/EAR files or specify the path to the JSP file.

3. Deploying to Tomcat
Ensure your Jenkins job is configured to deploy the JSP file to the Tomcat webapps directory. This can be done using the Deploy to container post-build action in Jenkins.

4. Monitoring Application Availability
Implement a monitoring solution to check the availability of your web application. This can be a simple script that periodically sends requests to your application's URL and checks for a successful response.
Alternatively, use monitoring tools like Nagios, Zabbix, or Prometheus to monitor your application's health and availability.
Validation
After setting up the Jenkins job and deploying the JSP file to Tomcat, access the web application through a browser by navigating to http://<Tomcat-Server-IP>:<Tomcat-Port>/<Your-JSP-AppName>/.

Ensure the application loads successfully and displays the expected content.

Troubleshooting
Deployment Issues: Check Jenkins and Tomcat logs for any errors related to deployment.
Application Not Available: Ensure Tomcat is running and accessible. Verify the JSP file is correctly deployed in the Tomcat webapps directory.
Conclusion
This exercise demonstrates the automation of deploying a JSP application using Jenkins and monitoring its availability. Such practices are crucial for maintaining the reliability and efficiency of web applications in a DevOps culture.
