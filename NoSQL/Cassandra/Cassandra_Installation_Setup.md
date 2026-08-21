# Apache Cassandra Installation & Setup (Docker)

## Objective

Set up Apache Cassandra locally using Docker Desktop and verify that it is running successfully.

---

# Prerequisites

- Windows 10/11
- Docker Desktop Installed
- Docker Engine Running
- Internet Connection

---

# Step 1 : Verify Docker Installation

Open Command Prompt.

```cmd
docker --version
```

Verify Docker Engine is running.

```cmd
docker ps
```

Expected Output

```text
CONTAINER ID   IMAGE   COMMAND   CREATED   STATUS   PORTS   NAMES
```

---

# Step 2 : Download Apache Cassandra Image

Download the latest Apache Cassandra 5.0 image.

```cmd
docker pull cassandra:5.0
```

Verify the image.

```cmd
docker images
```

Expected Output

```text
REPOSITORY   TAG
cassandra   5.0
```

---

# Step 3 : Create Cassandra Container

Create and start a Cassandra container.

```cmd
docker run -d --name cassandra -p 9042:9042 cassandra:5.0
```

Verify the container.

```cmd
docker ps
```

Expected Output

```text
CONTAINER ID   IMAGE           STATUS
xxxxxxxxxxxx   cassandra:5.0   Up xx seconds
```

---

# Step 4 : Verify Cassandra Startup

Check the container logs.

```cmd
docker logs -f cassandra
```

Wait until you see:

```text
Starting listening for CQL clients on /0.0.0.0:9042
Startup complete
Created default superuser role 'cassandra'
```

Press **Ctrl + C** to stop viewing logs.

> Note:
> This does **not** stop the Cassandra container.

---

# Step 5 : Connect using cqlsh

Open Cassandra Shell.

```cmd
docker exec -it cassandra cqlsh
```

Expected Output

```text
Connected to Test Cluster at 127.0.0.1:9042
[cqlsh 6.x | Cassandra 5.x | CQL spec 3.4.x]
```

You are now connected to your local Cassandra database.

---

# Step 6 : Verify Installation

Execute

```sql
DESCRIBE KEYSPACES;
```

Expected Output

```text
system
system_auth
system_distributed
system_schema
system_traces
```

---

# Step 7 : Exit cqlsh

```sql
EXIT;
```

or

```sql
QUIT;
```

---

# Docker Commands

Download Cassandra Image

```cmd
docker pull cassandra:5.0
```

Create and Start Container

```cmd
docker run -d --name cassandra -p 9042:9042 cassandra:5.0
```

View Running Containers

```cmd
docker ps
```

View All Containers

```cmd
docker ps -a
```

Connect to Cassandra

```cmd
docker exec -it cassandra cqlsh
```

View Logs

```cmd
docker logs cassandra
```

Follow Logs

```cmd
docker logs -f cassandra
```

Stop Container

```cmd
docker stop cassandra
```

Start Container

```cmd
docker start cassandra
```

Restart Container

```cmd
docker restart cassandra
```

Remove Container

```cmd
docker rm cassandra
```

Remove Image

```cmd
docker rmi cassandra:5.0
```

---

# Default Configuration

| Property | Value |
|----------|-------|
| Docker Image | cassandra:5.0 |
| Container Name | cassandra |
| Host | 127.0.0.1 |
| Port | 9042 |
| Cluster Name | Test Cluster |
| Shell | cqlsh |

---

# Installation Checklist

- [ ] Docker Desktop Installed
- [ ] Docker Engine Running
- [ ] Cassandra Image Downloaded
- [ ] Cassandra Container Created
- [ ] Cassandra Started Successfully
- [ ] Connected using cqlsh
- [ ] Verified using DESCRIBE KEYSPACES

---
