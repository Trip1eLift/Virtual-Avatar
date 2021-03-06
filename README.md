# Virtual-Avatar
A web-based virtual face renderer inspired by Vtuber.

Demo:![image](https://user-images.githubusercontent.com/43707388/156492954-dfb869b6-b473-4e2e-aabd-35ea9e3f5be6.png)


## Static site setup
Calibration is based on my personal Nexigo webcam.
```
cd standalone
npm install
npm run dev
```
Website is published on aws: https://virtualavatar.trip1elift.com/

Utilizing: Route53, Certs, CloudFront, S3

# 2 tier setup using websocket (old)
This project involves a Python Server running Mediapipe with Webcam to 3D scan the face. Then send the facial landmarks to Client using websocket protocol. The Client is built on react with graphics engine @react-three/fiber that render facial landmark into browser. This project requires Python3 and Node.js to run.

## Docker Start (camera issue, docker doesn't work.)
```console
docker-compose up -d 
```

## Dev Start
### 1. Python Server
To setup python virtual environment
```console
cd server
python3 -m venv ./venv
```

To activate
```console
where.exe python
./venv/Scripts/activate     (Windows)
source ./venv/bin/activate  (Mac)
where.exe python
```

Operations in venv
```console
pip list
pip install -r requirements.txt
```

```console
deactivate
```

### 2. React Client
To setup react environment
```console
cd client
npm install
```

To run
```console
yarn start
```
