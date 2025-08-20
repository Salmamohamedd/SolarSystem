# Dockerized Application

This repository contains a Dockerized version of the app, along with a CI workflow that automatically builds and pushes images to Docker Hub.

---

🐳 Docker Hub
-------------

Images are automatically built and pushed to Docker Hub on every commit to main.

*   docker pull username/app:latest
    
*   docker pull username/app:v1.0.0
    

⚙️ CI/CD
--------

*   On every push to main, GitHub Actions:
    
    *   Builds the Docker image
        
    *   Tags it as latest and with the commit/tag version
        
    *   Pushes it to Docker Hub (username/app)
        

Secrets required in the repo settings:

*   DOCKERHUB\_USERNAME
    
*   DOCKERHUB\_TOKEN
    

📖 How to Run
-------------
`   docker run -it --rm -p 3000:3000 username/app:latest   `
