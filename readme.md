# SE347 Project Documentation

## Overview

The SE347 project is a comprehensive task and project management system designed to enhance team collaboration and workflow. It consists of a **frontend** built with Next.js and TypeScript, and a **backend** developed using Spring Boot. The system supports key features such as user authentication, workspace management, project tracking, and task management.

## Technologies Used

- **Frontend**: Next.js, React, TypeScript, Tailwind CSS
- **Backend**: Spring Boot, Java, MinIO, JWT for authentication
- **Database**: MongoDB

## Key Features

### Frontend Features

1. **User Authentication**:
   - Sign up, Sign in, Edit profile
2. **Workspace Management**:
   - Create, join, and manage workspaces
3. **Project Management**:
   - Create, update, delete projects
4. **Task Management**:
   - Kanban board view
   - Calendar view for tasks
   - Task creation and editing

### Backend Features

1. **User Services**:
   - Manage user data and authentication (JWT-based)
2. **Workspace Services**:
   - Handle workspace creation, member management
3. **Project Services**:
   - CRUD operations for projects
4. **Task Services**:
   - CRUD operations for tasks
   - Support for task filtering and sorting
5. **MinIO Integration**:
   - File storage and retrieval through MinIO

## System Architecture

- **Frontend** communicates with **Backend** through RESTful APIs.
- **Backend** integrates with MongoDB for data persistence and MinIO for file storage.
- The system is containerized using Docker

## Setup Instructions

### Prerequisites

- Docker
- Docker compose

### Build the frontend and backend
```shell
 docker compose build
```
### Update the hosts file to ensure that services can be accesses correctly:
## Windows
1. Open NotePad as Administrator
2. Oepn the file located at C:\Windows\System32\drivers\etc\hosts.
3. Add the following lines at the end of the file:
```shell
127.0.0.1 minio
127.0.0.1 se347-backend
```
## Linux
1. Open a terminal and run the follwoing command to edit the hosts file
```shell
 sudo nano /etc/hosts
```
2. Add the following lines at the end of the files:
```shell
127.0.0.1 minio
127.0.0.1 se347-backend
```
3. Save and exit editor


### Run the applications
```shell
 docker compose up -d
```

## Backend API Documentation

The backend API documentation is available via Swagger at:

```
http://localhost:5000/ui-docs
```
## Access the frontend
```
http://localhost:4200
```

