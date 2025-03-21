# SPSP (Simple Photo Sharing Platform)
<img alt="Profile" width="500" src="https://github.com/user-attachments/assets/fb568197-ad6a-40b4-98b6-bbd64528529c" />
<img alt="Followings" width="500" src="https://github.com/user-attachments/assets/5494f1a3-8b83-4d1a-a8a2-52266e278318" />

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

# Screenshots

## Desktop

<img alt="SignIn" width="500" src="https://github.com/user-attachments/assets/35eeea74-511f-405d-9b65-aa4b9803629d" />
<img alt="SignUp" width="500" src="https://github.com/user-attachments/assets/27a10ca6-831a-45f3-a32b-df4ad08381ef" />

<img alt="ResetPassword" width="500" src="https://github.com/user-attachments/assets/3c73e039-9f68-4447-ba0c-5c71b4021b43" />
<img alt="News" width="500" src="https://github.com/user-attachments/assets/2573bf9a-ad2d-4926-af4d-7d8e31d5b5e1" />

<img alt="Profile" width="500" src="https://github.com/user-attachments/assets/b10dbd00-fa57-438c-b513-8129e9359097" />
<img alt="Followings" width="500" src="https://github.com/user-attachments/assets/182bd39f-e35f-4b87-82de-5de9eb2c3760" />

<img alt="Settings" width="500" src="https://github.com/user-attachments/assets/4f81634e-ca56-454c-b7ed-281386323182" />
<img alt="Post" width="500" src="https://github.com/user-attachments/assets/fdb8fc10-4528-4d7d-90a7-c1c0b1505c48" />

<img alt="DeletePost" width="500" src="https://github.com/user-attachments/assets/ecc554a4-4350-483c-8b14-f713851d8b7b" />
<img alt="EditPost" width="500" src="https://github.com/user-attachments/assets/73e05985-683a-490d-b7f4-9c60deaf98c7" />

<img alt="Likes" width="500" src="https://github.com/user-attachments/assets/50077b41-d936-4951-be6d-64d94aef399d" />
<img alt="Search" width="500" src="https://github.com/user-attachments/assets/3647542b-982d-454b-8f61-9ab1505e9f4b" />

## Mobile

<img alt="News 01" width="324" src="https://github.com/user-attachments/assets/1c772289-6dd2-427a-9b9b-34f927aa639b" />
<img alt="News 02" width="324" src="https://github.com/user-attachments/assets/2c530d42-dd51-4314-b3fb-96c730ca6328" />
<img alt="Profile 01" width="324" src="https://github.com/user-attachments/assets/98bcc6e7-f957-421a-9401-719afd61b703" />

<img alt="Followings" width="324" src="https://github.com/user-attachments/assets/fe77d928-523f-4579-9147-cc8da607200f" />
<img alt="Settings Menu" width="324" src="https://github.com/user-attachments/assets/0100d252-210b-47d6-9f47-a917c98c83b8" />
<img alt="Settings" width="324" src="https://github.com/user-attachments/assets/04d37530-3517-401b-8170-c167da4b409a" />

<img alt="Search" width="324" src="https://github.com/user-attachments/assets/9b1db0a1-e22f-46a5-a009-e23cc739290b" />
<img alt="Profile 02" width="324" src="https://github.com/user-attachments/assets/5e2a0ccd-1c12-4e0b-8205-d1ab48a49951" />
<img alt="Post 01" width="324" src="https://github.com/user-attachments/assets/e729564f-5d8a-42b6-a4fd-0aca8000634d" />




