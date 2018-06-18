# Build Docker Image

git clone https://github.com/aliouba/flask-docker.git

cd flask-docker

docker build -t flask-demo:latest .

# Start Flask Container

docker run -d -p 5000:5000 --name flask1 flask-demo

# Rebuild

docker build -t flask-demo:latest

docker rm -f flask1

docker run -d -p 5000:5000 --name flask1 flask-demo

