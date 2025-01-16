# SocialSphere: A Multi-Tier Web Application

## Project Overview
**SocialSphere** is a scalable, automated, and multi-tier social networking web application designed for seamless performance and optimized resource management. Built with Java and Maven, the project employs Infrastructure as Code (IaC) principles to ensure repeatable and automated deployment. 

This application integrates Nginx, Tomcat, RabbitMQ, Memcached, MySQL, and NFS for external storage, providing a robust platform to support dynamic user interactions and data management.

---

## Architecture Diagram
Below is the architectural blueprint of the SocialSphere application stack:

![Architecture Diagram](./architecture_diagram.png)

---

## Features
- **Scalability**: Multi-tier architecture ensures smooth scaling.
- **Automation**: Fully automated setup using IaC for repeatable deployments.
- **Efficiency**: Optimized caching and message queuing mechanisms.
- **Persistence**: NFS for external storage to handle large data volumes.
- **Robust Backend**: Java-based application built with Maven for dependency management.

---

## Tools and Technologies
| **Component**      | **Technology**  | **Purpose**                                                                 |
|---------------------|-----------------|-----------------------------------------------------------------------------|
| **Frontend**       | Nginx           | Acts as a reverse proxy and load balancer.                                 |
| **Backend**        | Tomcat          | Hosts the Java-based web application.                                      |
| **Queue System**   | RabbitMQ        | Facilitates asynchronous messaging between components.                     |
| **Caching**        | Memcached       | Caches frequently accessed data to reduce database load.                   |
| **Database**       | MySQL           | Manages persistent user and application data.                              |
| **Storage**        | NFS             | Provides external shared storage for scalability and reliability.          |
| **Build Tool**     | Maven           | Manages dependencies and builds the Java-based application.                |

---

## Prerequisites
1. Virtualization software or cloud environment for deployment (e.g., VirtualBox, AWS).
2. Infrastructure automation tools (e.g., Ansible, Terraform).
3. Basic knowledge of Java, Maven, and Linux.

---

## Setup Instructions
### 1. Clone the Repository
```bash
$ git clone https://github.com/your-username/SocialSphere.git
$ cd SocialSphere
```

### 2. Infrastructure Setup
Use IaC tools to provision the required servers:
- **Web Layer**: Deploy Nginx for load balancing and routing.
- **Application Layer**: Set up Tomcat to host the Java WAR file.
- **Data Layer**: Configure MySQL, RabbitMQ, Memcached, and NFS services.

### 3. Build the Application
```bash
$ mvn clean install
```
The build process generates a WAR file in the `target` directory.

### 4. Deploy the Application
1. Copy the WAR file to the Tomcat webapps directory.
2. Start the Tomcat service:
```bash
$ systemctl start tomcat
```

### 5. Configure Nginx
Set up Nginx to proxy requests to Tomcat and configure SSL (if needed).

### 6. Access the Application
Navigate to the public IP of the web server in your browser to access the SocialSphere application.

---

## Directory Structure
```
SocialSphere/
├── src/                   # Source code for the application
├── pom.xml                # Maven project file
├── docs/                  # Documentation and architecture diagram
├── ansible/               # IaC configurations
└── README.md              # Project overview and setup instructions
```

---

## Future Enhancements
- Implement Kubernetes for container orchestration.
- Add CI/CD pipelines using Jenkins or GitHub Actions.
- Enhance scalability with horizontal scaling for application and data layers.

---

## Contributing
Contributions are welcome! Please fork the repository and submit a pull request with your changes.

---

## License
This project is licensed under the [MIT License](./LICENSE).

---

## Acknowledgments
Special thanks to the open-source community and developers of the technologies utilized in this project.

---

**Happy Coding!** 🚀
