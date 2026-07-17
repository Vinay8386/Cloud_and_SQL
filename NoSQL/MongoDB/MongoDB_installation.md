# MongoDB Installation & Setup

## Objective

-   Install MongoDB Community Server.
-   Install MongoDB Compass.
-   Install MongoDB Shell (mongosh).
-   Verify that MongoDB Server is running.
-   Connect to the local MongoDB instance.

------------------------------------------------------------------------

## Step 1: Install MongoDB Community Server

-   Download MongoDB Community Server from the official website:
    -   https://www.mongodb.com/try/download/community
-   Install using the default settings.
-   During installation:
    -   Install MongoDB as a Windows Service.
    -   Keep **Install MongoDB Compass** checked.

**Default Installation Location**

``` text
C:\Program Files\MongoDB\Server\<version>\
```

------------------------------------------------------------------------

## Step 2: Verify MongoDB Server Installation

Open:

``` text
C:\Program Files\MongoDB\Server\<version>\bin
```

Verify the following files exist:

``` text
mongod.exe
mongos.exe
```

Start MongoDB Compass.

Connection String:

``` text
mongodb://localhost:27017
```

If the connection is successful, MongoDB Server is running correctly.

------------------------------------------------------------------------

## Step 3: Install MongoDB Compass (If Not Installed)

Download MongoDB Compass:

-   https://www.mongodb.com/try/download/compass

Install using the default settings.

Purpose:

-   Official GUI for MongoDB.
-   Used to visualize databases, collections, documents, indexes, and
    execute queries visually.

------------------------------------------------------------------------

## Step 4: Install MongoDB Shell (mongosh)

MongoDB Community Server does **not** install mongosh automatically.

Download MongoDB Shell:

-   https://www.mongodb.com/try/download/shell

Choose:

-   Platform: Windows
-   Package: MSI
-   Version: Latest Stable

Install using the default settings.

**Default Installation Location**

``` text
C:\Program Files\mongosh\
```

------------------------------------------------------------------------

## Step 5: Verify mongosh Installation

Open **Command Prompt**.

Execute:

``` bash
mongosh
```

Expected Output:

``` text
Using MongoDB: 8.x.x
Using Mongosh: 2.x.x

test>
```

`test>` indicates that mongosh has successfully connected to the local
MongoDB server.

------------------------------------------------------------------------

## Folder Structure

``` text
C:\Program Files\
├── MongoDB
│   └── Server
│       └── <version>
│           └── bin
│               ├── mongod.exe
│               └── mongos.exe
│
└── mongosh
    └── mongosh.exe
```

------------------------------------------------------------------------

## Components

### MongoDB Community Server

Purpose:

-   MongoDB Database Server.

Executable:

``` text
mongod.exe
```

------------------------------------------------------------------------

### MongoDB Compass

Purpose:

-   Official GUI Client.
-   Used to manage MongoDB visually.

------------------------------------------------------------------------

### MongoDB Shell (mongosh)

Purpose:

-   Official Command Line Client.
-   Used to execute MongoDB commands from the terminal.

------------------------------------------------------------------------

### mongos.exe

Purpose:

-   Query Router used in MongoDB Sharding.
-   Not used in standalone MongoDB installations.

------------------------------------------------------------------------

## Installation Summary

  Component                  Purpose
  -------------------------- ---------------------
  MongoDB Community Server   Database Server
  MongoDB Compass            GUI Client
  mongosh                    Command Line Client

------------------------------------------------------------------------

## Interview Questions

### What are the three components required for MongoDB development?

-   MongoDB Community Server
-   MongoDB Compass
-   MongoDB Shell (mongosh)

### Is mongosh installed automatically with MongoDB Community Server?

No. It must be installed separately.

### What is the purpose of MongoDB Compass?

GUI tool used to visualize and manage MongoDB.

### What is the purpose of mongosh?

Command-line shell used to execute MongoDB commands.

### What is the purpose of mongod.exe?

Starts and runs the MongoDB Database Server.

### What is the purpose of mongos.exe?

Query Router used in MongoDB Sharding. It is not used in standalone
MongoDB installations.