# Deploy Simple Website

## Description
This project is a simple DevOps pipeline for deploying a static HTML website using Nginx. It demonstrates the use of Docker and Jenkins for continuous integration and deployment.

## Technologies Used
- Docker
- Jenkins
- Nginx
- HTML

## Setup Instructions
1. Clone the repository:
   ```bash
   git clone https://github.com/ibrahimelothmani/Deploy-Simple-Website.git
   cd Deploy-Simple-Website
   ```
2. Build the Docker image:
   ```bash
   docker build -t simple-website .
   ```
3. Run the Docker container:
   ```bash
   docker run -d -p 80:80 simple-website
   ```

## Usage
Access the website by navigating to `http://localhost` in your web browser.

## Screenshots
### Pipeline Overview
![Pipeline Overview](Pipeline%20overview.png)

### Website Overview
![Website Overview](website%20overview.png)

## License
This project is licensed under the MIT License.
