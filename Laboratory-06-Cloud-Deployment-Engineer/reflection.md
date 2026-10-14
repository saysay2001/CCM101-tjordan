# Mission Reflection – Laboratory 06: The Cloud Deployment Engineer

Writing a `docker-compose.yml` file made me realize how much easier it is to manage cloud applications using automation. Instead of manually typing commands to create and configure each container, I can define the services, environment variables, ports, and other settings in one file. This saves time, reduces repetitive work, and makes the deployment easier to reproduce and maintain.

I also learned that YAML indentation is very important. YAML uses spaces to organize its structure, so using a Tab instead of spaces or placing the wrong number of spaces can cause errors. Docker Compose might fail to read the configuration file or may not interpret the settings correctly. This taught me to be careful when writing code and to check the configuration before deploying an application.

Environment variables, such as `MYSQL_PASSWORD`, are used to provide configuration values to containers. They help separate application settings from the container image and allow services to use the correct database credentials. However, I learned that passwords should be handled carefully because environment variables in a Compose file are not automatically encrypted. For better security, sensitive information should be stored using appropriate secrets management practices.

Deploying Nextcloud in just a few minutes was an exciting experience. I was surprised that I could set up a private cloud storage system using only a few commands and a configuration file. It helped me understand how modern cloud applications can be deployed efficiently without manually configuring every component.

Since Mission 1, my understanding of cloud computing has improved. I previously viewed cloud computing mainly as accessing files and services through the internet. Now, I understand that it also involves infrastructure, containers, networking, storage, automation, and system management. This mission showed me that cloud engineers need both technical knowledge and attention to detail to build reliable services. Overall, I gained practical experience and a better appreciation of how automation simplifies cloud deployment.
