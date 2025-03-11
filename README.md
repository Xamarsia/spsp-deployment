
Demo: https://spspdemo.online/


# Description

Simple social network for photo sharing (Instagram like). The platform is a microservice client-server application that is implemented using Spring framework on backend and Next.js framework on frontend.

This project consists of [backend](https://github.com/Xamarsia/simple-photo-sharing-platform),  [frontend](https://github.com/Xamarsia/photo-sharing-platform-frontend) services. Also it utilizes Firebase Auth and Amazon S3. 

Backend is stateless and implemented as REST API.

Development stack:
- Frontend: Typescript (React, Next.js, Zod), HTML, CSS (Tailwind CSS), Firebase Auth.
- Backend: Java (Spring), SQL (PostgreSQL), Amazon S3.
- General: Git(GitHub), Jira, Docker, Kubernetes, Figma, Visual Studio Code.

Links: 
- Frontend: https://github.com/Xamarsia/photo-sharing-platform-frontend
- Backend: https://github.com/Xamarsia/simple-photo-sharing-platform



# Requirements

- Linux (Ubuntu/Debian)
- Visual Studio Code (`ms-vscode-remote.remote-containers` extension)
- Docker Engine


# Installation

## Setup environment
1. Install Visual Studio Code (`ms-vscode-remote.remote-containers` extension)
2. Install Docker Engine  [Install Docker Engine on Ubuntu](https://docs.docker.com/engine/install/ubuntu/#install-using-the-repository) and  [Linux post-installation steps for Docker Engine](https://docs.docker.com/engine/install/linux-postinstall/)  
3. Create docker network:
```bash
docker network create microservice_network
```

4. Clone a Project with [Submodules](https://git-scm.com/book/en/v2/Git-Tools-Submodules)
```bash 
git clone --recurse-submodules https://github.com:Xamarsia/spsp-deployment.git
cd spsp-deployment

# Pulling in Upstream Changes from the Submodule Remote
git submodule update --remote

# Update the commits
git add photo-sharing-platform-frontend
git commit -m 'Update gitlink to photo-sharing-platform-frontend'
git push origin 
```

## Setup AWS

### Setup IAM.
1. Create user with `AmazonS3FullAccess` permission.
2. Create access key in user security credentials save `Access key` and `Secret access key` for the future process.
### Setup S3:
1. Create `profiles` and `posts` buckets.

## Setup Firebase
### [Log in to Firebase](https://firebase.google.com/codelabs/firebase-nextjs#1)
### [Create a Firebase project](https://firebase.google.com/codelabs/firebase-nextjs#2)
### [Add a web app to your Firebase project](https://firebase.google.com/codelabs/firebase-nextjs#2)



