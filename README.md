# Group Trip Planner

**Team Name:** Team Mongoose

### Members
|  zID    |  Name |
| :------------- | :----------: | 
|  z5251839 |  Aadhishrii Patiil |
|  z5319999  |  Enoch  Luu |
|  z5261844 | Huiyi (Tanya) Wang | 
|  z5207855 | Sanojan Thiyagaraja | 
|  z5208105| Tingzhuang (Sam) Zhou  | 


<br>

## How To Run
## Run with Docker
### Install Docker
For Mac: https://docs.docker.com/docker-for-mac/install/ <br>
For Windows: https://docs.docker.com/docker-for-windows/install/ <br>
For Ubuntu: https://docs.docker.com/engine/install/ubuntu/
### Build Docker image
```
docker build -t trip_collab .
```
### Start a Docker container running the service
```
docker run -itd -p 3000:3000 -p 5000:5000 --name mongoose_demo trip_collab
```
The service will start in 2 minutes, then you can open [http://localhost:3000](http://localhost:3000) with your browser to visit our website.

### Enter the container
```
docker exec -it mongoose_demo bash
```

## Run on Your Local Machine
## Backend
### Install PostgreSQL
Please refer to https://www.postgresql.org/download/ .

### Initialise PostgreSQL database
```
service postgresql start
createdb trip_collab
psql trip_collab < backend/data.sql
```

### Install Redis
```
apt install redis-server
```

### Start Redis service
```
service redis-server start
```
or
```
systemctl start redis
```
### Install Python packages
```
pip install -r backend/requirements.txt
```
### Run Flask server
```
python3 backend/api/server.py
```
## Frontend
### Install npm
Please refer to https://nodejs.org/en/download/ .

### Install all dependencies and run the development server
```
cd frontend
npm install
```

```bash
npm run dev
# or
yarn dev
```
Open [http://localhost:3000](http://localhost:3000) with your browser to see the result.

