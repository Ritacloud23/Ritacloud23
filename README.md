# Rita Nnenna — Cloud & DevOps Engineer

![Cloud DevOps Banner](https://images.unsplash.com/photo-1461749280684-dccba630e2f6?auto=format&fit=crop&w=1200&q=80)

## About Me

I’m a Cloud & DevOps Engineer with hands-on experience in deploying, automating, and managing cloud infrastructures on AWS. I specialize in containerization (Docker), orchestration (Kubernetes), CI/CD pipelines (GitHub Actions, Jenkins), and Infrastructure as Code (Terraform, Ansible) to deliver scalable, reliable, and secure cloud-based applications.


## Technical Skills

- **Cloud Platforms:** AWS (EC2, S3, ECR, VPC, Route 53, CloudFront, IAM, CloudWatch)
- **Containers & Orchestration:** Docker, Kubernetes (EKS), Portainer
- **CI/CD:** Git & GitHub Actions, Jenkins
- **Infrastructure as Code:** Terraform, Ansible
- **Networking:** Nginx, HAProxy (Load Balancing & Reverse Proxy)
- **OS & Scripting:** Linux Server Management, Bash Scripting
- **Security:** SSL Configuration (Certbot / Let’s Encrypt)
- **Monitoring:** Datadog, CloudWatch, Pathamus Agranafaner


## Soft Skills

- Problem Solving & Troubleshooting
- Communication & Team Collaboration
- Technical Documentation (Notion & GitHub)
- Continuous Learning & Adaptability
- Attention to Detail & Time Management


## Favorite Projects

### [Medplus Cloud Deployment Project](https://github.com/Ritacloud23/medplus-cloud-deployment)
A 3-tier web app deployed on AWS using Docker, GitHub Actions, ECR, and EC2 with SSL-enabled HAProxy reverse proxy.

### [Registration-App (FastAPI + React)](https://github.com/Ritacloud23/registration-app)
A containerized application showcasing full-stack deployment with CI/CD automation.

### [Medilab Portfolio Site](https://github.com/Ritacloud23/medilab-portfolio)
A personal portfolio hosted on AWS S3 + CloudFront with custom domain and responsive design.


## Certifications & Achievements

- **AWS Cloud Practitioner**
- ** DigitalWitch Academy — Cloud computing **


## Fun Fact / Unique Side

When I’m not automating deployments, I enjoy creating clean documentation in Notion, designing DevOps visuals in Canva, and mentoring others learning AWS and Docker.  
I believe in simplifying tech — making cloud engineering easy to understand for everyone.

## Connect With Me
 [Portfolio](https://ritacloudsolutuin.online)
 [LinkedIn](https://linkedin.com/in/rita-nnenna)
 [GitHub](https://github.com/Ritacloud23)https:
 [X]https://x.com/RitaNnenna5?t=4wBPMdEEnpz6W1soN3E1Jw&s=09
  ugwuanyinnenna43@gmail.com


## Sample Code Blocks

### Dockerfile Example

```dockerfile
FROM python:3.10-slim
WORKDIR /app
COPY . /app
RUN pip install -r requirements.txt
CMD ["uvicorn", "main:app", "--host", "0.0.0.0", "--port", "80"]
```

### Terraform AWS EC2 Example

```hcl
resource "aws_instance" "web" {
  ami           = "ami-0c55b159cbfafe1f0"
  instance_type = "t2.micro"

  tags = {
    Name = "WebServer"
  }
}
```

### GitHub Actions CI/CD Workflow

```yaml
name: CI/CD Pipeline
on: [push]
jobs:
  build-deploy:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v3
      - name: Build Docker Image
        run: docker build -t ${{ secrets.DOCKER_IMAGE }} .
      - name: Deploy to AWS ECR
        run: |
          aws ecr get-login-password | docker login --username AWS --password-stdin ${{ secrets.AWS_ECR_URL }}
          docker push ${{ secrets.AWS_ECR_URL }}/${{ secrets.DOCKER_IMAGE }}
```
