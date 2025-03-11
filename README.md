<img alt="Profile 01" width="500" src="https://github.com/user-attachments/assets/2d807ad7-1a17-49cf-8a9d-3bec3a5ed911" />
<img alt="Followings" width="500" src="https://github.com/user-attachments/assets/1a2cd37e-eea9-4264-85ac-7f03fe2a3433" />

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

# Screenshots

## Desktop

<img alt="Profile 02" width="500" src="https://github.com/user-attachments/assets/5cec0da3-58a6-490b-a0d4-d693bb3f419c" />
<img alt="Settings" width="500" src="https://github.com/user-attachments/assets/ffd08918-6126-407a-bbbf-5c270c2118fe" />

<img alt="Post 01" width="500" src="https://github.com/user-attachments/assets/cde0b1f1-681f-4ec7-9a34-763ce2b5d13f" />
<img alt="Delete post" width="500" src="https://github.com/user-attachments/assets/b56d01b4-aff2-4584-a811-d192c3a02741" />

<img alt="Post 02" width="500" src="https://github.com/user-attachments/assets/0fa5c64f-e6d7-44ee-8520-b16f3d47cbdc" />
<img alt="Likes list" width="500" src="https://github.com/user-attachments/assets/c1bff84d-3edb-4c29-8613-11932575d2f0" />

<img alt="Search" width="500" src="https://github.com/user-attachments/assets/8c570b6a-3d6b-4877-b678-aba2f695b461" />
<img alt="Create post" width="500" src="https://github.com/user-attachments/assets/95c26e30-0dbb-4eac-aaee-a364138a711d" />


<img alt="ResetPassword" width="500" src="https://github.com/user-attachments/assets/33720a15-138a-41fd-986d-cf8ce56167ae" />
<img alt="News" width="500" src="https://github.com/user-attachments/assets/485cc052-1840-4b12-bb65-c35b34f76d22" />

<img alt="SignIn" width="500" src="https://github.com/user-attachments/assets/9ed891e9-3f3f-4d46-9b13-3f8777ee576a" />
<img alt="SignUp" width="500" src="https://github.com/user-attachments/assets/55a08fd4-2ee1-4463-9b92-ced71fa907f3" />



## Mobile

<img alt="Smartphone Profile 01" height="600" src="https://github.com/user-attachments/assets/c0418783-2d0f-4ee0-9831-d4fffd6adc4d" />
<img alt="Smartphone Followings" height="600" src="https://github.com/user-attachments/assets/89caaa53-e7c8-49a1-a91e-38b672975599" />
<img alt="Smartphone Settings Menu" height="600" src="https://github.com/user-attachments/assets/36ac41ec-7c56-4e9d-9258-57d29eae064a" />

<img alt="Smartphone Settings" height="600" src="https://github.com/user-attachments/assets/77a401c2-0d07-4b9c-b33e-feee9cb1c33e" />
<img alt="Smartphone Profile 02" height="600" src="https://github.com/user-attachments/assets/b31ee3d5-1cea-43a6-b9f9-337f8d274836" />
<img alt="Smartphone Post 01" height="600" src="https://github.com/user-attachments/assets/b572dd06-e56e-417b-aa55-2275496779cc" />

<img alt="Smartphone News 02" height="600" src="https://github.com/user-attachments/assets/bf1574ad-54b7-406c-939d-f4a158e9047d" />
<img alt="Smartphone News 01" height="600" src="https://github.com/user-attachments/assets/0155816c-29fc-4522-bc42-045bb66fcb33" />



