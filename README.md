# Flask-ops


## Steps to Build and Run the Docker Container:
1. Build the Docker Image:
```bash
docker build -t flask-app .
```
2. Run the Docker Container:
```bash
docker run -p 8000:8000 flask-app
```
## 

If you want to run a security scan for container:
```bash
docker run --rm -v /var/run/docker.sock:/var/run/docker.sock aquasec/trivy image flask-app
```

##
Use Static Application Security Testing (SAST) tools like Bandit to find security issues in Python code:
```bash
pip install bandit
bandit -r app.py
```

##
Run the following command to generate the certificate and private key:
```bash
openssl req -x509 -newkey rsa:4096 -nodes -keyout key.pem -out cert.pem -days 365
```
- `key.pem`: This is your private key.
- `cert.pem`: This is your self-signed certificate.
- `days 365`: This sets the certificate to expire in 1 year.