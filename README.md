<h1 align="center">
  <p>Simple Photo Sharing Platform (SPSP)</p>
  <br>
  	<p align="center">
	    <img alt="Profile" width="45%" src="https://github.com/user-attachments/assets/fb568197-ad6a-40b4-98b6-bbd64528529c" />
	    <img alt="Followings" width="45%" src="https://github.com/user-attachments/assets/5494f1a3-8b83-4d1a-a8a2-52266e278318" />
	</p>
	<h4 align="left">Demo: https://spspdemo.online/</h4>

The Simple Photo Sharing Platform (SPSP) is a web-based social media platform.
It provides a user-friendly interface for content sharing and profile management.

SPSP compatible with various devices to ensure a smooth user experience.

</h1>

## Table Of Content

- [Description](#description)
- [Services](#services)
- [Features](#features)
	- [Key Features](#key-features)
	- [Security Features](#security-features)
- [Installation](#installation)
    - [Setup environment](#setup-environment)
    - [Setup AWS](#setup-aws)
        - [Setup IAM](#setup-iam)
        - [Setup S3](#setup-s3)
    - [Setup Firebase](#setup-firebase)
- [Screenshots](#screenshots)
    - [Desktop](#desktop)
    - [Mobile](#mobile)
- [Future Enhancements](#future-enhancements)
- [License](#license)

## Description

Simple Photo Sharing Platform (SPSP) is a microservice client-server application.
It designed to foster user interaction and content sharing.

Users can create customizable profiles that shows their personality through profile picture, bios, and a collection of their posts.

The platform encourages social connectivity with follow and unfollow functionalities, allowing users to curate their feeds based on their interests and relationships.

A search feature enables users to find others by username or full name, making it easy to connect with friends and discover new accounts.

SPSP offers an intuitive interface for content sharing, allowing users to create, update, and delete posts effortlessly.

Engagement is enhanced by the inclusion of like and dislike features, which promote a sense of community and allow feedback on shared content.

Platform are web-based and developt to be compatible with various devices. See [Screenshots](./Screenshots) for more details.

This project consists of [backend](https://github.com/Xamarsia/simple-photo-sharing-platform) and [frontend](https://github.com/Xamarsia/photo-sharing-platform-frontend) services. See [Services](./Services) for more details.

## Services

- [`photo-sharing-platform-frontend`](https://github.com/Xamarsia/photo-sharing-platform-frontend): frontend, implemented using Next.js framework.

Frontend developed with Typescript. Frontend components are stateless.

- [`simple-photo-sharing-platform`](https://github.com/Xamarsia/simple-photo-sharing-platform): backend, implemented using Spring framework.

Backend is stateless and implemented as REST API.

## Features

### Key Features

- __User Authentication:__ Sign In, Sign Up, and Sign Out system. Password reset option.
- __User Profiles:__ Customizable profiles with profile picture, bios and posts.
- __User Interaction:__  Follow and unfollow functionality.
- __User Search:__ Search for users by username or full name.
- __Content Sharing:__ Intuitive interface for creating, updating, or deleting posts.
- __Content Interaction:__ Like and dislike functionality for user engagement.
- __News Page:__ Posts page.
- __Device Compatibility:__ Compatible with various devices to ensure a smooth user experience.
  
### Security Features

- Authentication using email addresses and passwords or popular identity provider Google. It is implemented by using Firebase Authentication and it leverages industry standards like OAuth 2.0.
- Custom exception handler to identify and debug errors.
- Using DTOs to encapsulate data and transport it without any business logic.
- Implemented strict form validations on the frontend. Inforced strict input validation on the backend.

## Development stack

### Frontend

- `Next.js` ( React ) - React framework that enables client and server rendering, advanced routing, nested layouts, data fetching.
- `TypeScript` for static type checking.
- `Tailwind CSS` for CSS styling.
- `Zod` for forms validation.
- `Firebase Auth` for providing security authentication.

### Backend

- `Spring` - for quickly build standalone backend application. Spring prowides dependency injection, auto-configuration, security features  and simplifies database integration.
- `Jakarta Validation` - to write constraints on object models via annotations.
- `Hibernate ORM` simplifies database interactions by mapping Java objects to database tables.
- `PostgreSQL` used as main database. Stores posts and users information.
- `Amazon S3` used as image storage (for posts and users).
- `Flyway`  control main database(postgresql) migration scripts.
- `JUnit` is used to write unit tests.
- `Mockito` - mocking framework for unit tests.

### General

- `Docker` - helps create and manage an isolated environment for building, sharing, and running applications.
- `Kubernetes` for deploying and managing containerized applications.
- `Visual Studio Code` provide customizeble development environment.
- `Jira` for project management and task tracking.
- `Figma` for project prototyping.
- `GitHub` (`Git`) - for code storage, sharing, and management.

## Installation

### Setup environment

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

### Setup AWS

#### Setup IAM

1. Create user with `AmazonS3FullAccess` permission.
2. Create access key in user security credentials save `Access key` and `Secret access key` for the future process.

#### Setup S3

1. Create `profiles` and `posts` buckets.

### Setup Firebase

1. [Log in to Firebase](https://firebase.google.com/codelabs/firebase-nextjs#1)
2. [Create a Firebase project](https://firebase.google.com/codelabs/firebase-nextjs#2)
3. [Add a web app to your Firebase project](https://firebase.google.com/codelabs/firebase-nextjs#2)

## Screenshots

### Desktop

<p align="center">
	<img alt="SignIn" width="48%" src="https://github.com/user-attachments/assets/35eeea74-511f-405d-9b65-aa4b9803629d" />
	<img alt="SignUp" width="48%" src="https://github.com/user-attachments/assets/27a10ca6-831a-45f3-a32b-df4ad08381ef" />
	<img alt="ResetPassword" width="48%" src="https://github.com/user-attachments/assets/3c73e039-9f68-4447-ba0c-5c71b4021b43" />
	<img alt="News" width="48%" src="https://github.com/user-attachments/assets/2573bf9a-ad2d-4926-af4d-7d8e31d5b5e1" />
	<img alt="Profile" width="48%" src="https://github.com/user-attachments/assets/b10dbd00-fa57-438c-b513-8129e9359097" />
	<img alt="Followings" width="48%" src="https://github.com/user-attachments/assets/182bd39f-e35f-4b87-82de-5de9eb2c3760" />
	<img alt="Settings" width="48%" src="https://github.com/user-attachments/assets/4f81634e-ca56-454c-b7ed-281386323182" />
	<img alt="Post" width="48%" src="https://github.com/user-attachments/assets/fdb8fc10-4528-4d7d-90a7-c1c0b1505c48" />
	<img alt="DeletePost" width="48%" src="https://github.com/user-attachments/assets/ecc554a4-4350-483c-8b14-f713851d8b7b" />
	<img alt="EditPost" width="48%" src="https://github.com/user-attachments/assets/73e05985-683a-490d-b7f4-9c60deaf98c7" />
	<img alt="Likes" width="48%" src="https://github.com/user-attachments/assets/50077b41-d936-4951-be6d-64d94aef399d" />
	<img alt="Search" width="48%" src="https://github.com/user-attachments/assets/3647542b-982d-454b-8f61-9ab1505e9f4b" />
</p>

### Mobile

<p align="center">
	<img alt="News 01" width="32%" src="https://github.com/user-attachments/assets/1c772289-6dd2-427a-9b9b-34f927aa639b" />
 	<img alt="News 02" width="32%" src="https://github.com/user-attachments/assets/2c530d42-dd51-4314-b3fb-96c730ca6328" />
	<img alt="Profile 01" width="32%" src="https://github.com/user-attachments/assets/98bcc6e7-f957-421a-9401-719afd61b703" />
	<img alt="Followings" width="32%" src="https://github.com/user-attachments/assets/fe77d928-523f-4579-9147-cc8da607200f" />
 	<img alt="Settings Menu" width="32%" src="https://github.com/user-attachments/assets/0100d252-210b-47d6-9f47-a917c98c83b8" />
	<img alt="Settings" width="32%" src="https://github.com/user-attachments/assets/04d37530-3517-401b-8170-c167da4b409a" />
	<img alt="Search" width="32%" src="https://github.com/user-attachments/assets/9b1db0a1-e22f-46a5-a009-e23cc739290b" />
	<img alt="Profile 02" width="32%" src="https://github.com/user-attachments/assets/5e2a0ccd-1c12-4e0b-8205-d1ab48a49951" />
	<img alt="Post 01" width="32%" src="https://github.com/user-attachments/assets/e729564f-5d8a-42b6-a4fd-0aca8000634d" />
</p>

## Future Enhancements

- Utilizing Nginx Ingress Controller as a reverse proxy and load balancer.
- Utilizing `slf4j` logging.
- Adding functionality for comments and tags.

## License

Licensed under the MIT License. See [LICENSE](./LICENSE) file for more details.
