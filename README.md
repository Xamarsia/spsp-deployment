<h1 align="center">
  <p>Simple Photo Sharing Platform (SPSP)</p>
  <br>
   <p align="center">
     <img alt="Profile" width="45%" src="https://github.com/user-attachments/assets/fb568197-ad6a-40b4-98b6-bbd64528529c" />
     <img alt="Followings" width="45%" src="https://github.com/user-attachments/assets/5494f1a3-8b83-4d1a-a8a2-52266e278318" />
 </p>
</h1>

__Demo: [spspdemo.online](https://spspdemo.online/)__

The Simple Photo Sharing Platform (SPSP) is a web-based social media platform.
It provides an interface for content sharing and profile management.
SPSP compatible with various devices to ensure a smooth user experience.

## Table Of Content

- [Description](#description)
- [Services](#services)
- [Development Stack](#development-stack)
  - [Frontend](#frontend)
  - [Backend](#backend)
  - [Common](#common)
- [Features](#features)
- [AWS Setup](#aws-setup)
- [Firebase Setup](#firebase-setup)
- [Environment Setup](#environment-setup)
- [Build & Run](#build--run)
- [UI Prototype](#ui-prototype)
  - [UI Prototype V 1.0 Smartphone](#ui-prototype-v-10-smartphone)
  - [UI Prototype V 1.0 PC](#ui-prototype-v-10-pc)
- [Screenshots](#screenshots)
  - [Desktop](#desktop)
  - [Mobile](#mobile)
- [Future Enhancements](#future-enhancements)
- [License](#license)

## Description

Simple Photo Sharing Platform (SPSP) is a microservice client-server application.

Users can create customizable profiles that shows their personality through profile picture, bios, and a collection of their posts.

The platform encourages social connectivity with follow and unfollow functionalities, allowing users to curate their feeds based on their interests and relationships.

A search feature enables users to find others by username or full name, making it easy to connect with friends and discover new accounts.

SPSP offers an intuitive interface for content sharing, allowing users to create, update, and delete posts effortlessly.

Engagement is enhanced by the inclusion of like and dislike features, which promote a sense of community and allow feedback on shared content.

Platform are web-based and developed to be compatible with various devices.

This project consists of [backend](https://github.com/Xamarsia/simple-photo-sharing-platform) and [frontend](https://github.com/Xamarsia/photo-sharing-platform-frontend) services. See [Services](./Services) for more details.

## Services

- [`photo-sharing-platform-frontend`](https://github.com/Xamarsia/photo-sharing-platform-frontend): frontend, implemented using Typescript and Next.js ( React ) framework.

- [`simple-photo-sharing-platform`](https://github.com/Xamarsia/simple-photo-sharing-platform): backend, stateless and implemented as REST API using Java and the Spring framework.

## Development Stack

### Frontend

- `Next.js` ( React ) - for client and server rendering, advanced routing, nested layouts, data fetching.
- `TypeScript` - for static type checking.
- `Tailwind CSS` - for simplified CSS styling.
- `ESLint` - for code linting.
- `Zod` - for frontend forms validation.
- `Firebase Auth` - for providing security authentication.
- `Figma` - for project prototyping.

### Backend

- `Spring` - main development framework. Used for dependency injection, auto-configuration, security features and simplified database integration.
- `Jakarta Validation` - to write constraints on object models via annotations.
- `Hibernate ORM` - to simplify database interactions by mapping Java objects to database tables.
- `PostgreSQL` - used as the main database. Stores posts and users information.
- `Amazon S3` - used for image storage (for posts and user profiles).
- `Flyway` - manages database migration scripts for PostgreSQL.
- `JUnit` - to write unit tests.
- `Mockito` - to write mocks for unit tests.

### Common

- `Docker` - for isolated development environment and deployment.
- `Kubernetes` - for deploying and managing containerized application.
- `Visual Studio Code`- preferred IDE for development.
- `Jira` - for project management and task tracking.

## Features

- __User Authentication:__ Sign In, Sign Up, and Sign Out functionalities, including password reset option.
  - Supports authentication via email and password or external identity provider ( Google ).
- __Unauthorized Preview:__ Non-authenticated users can view a news feed, posts, and other user's profiles.
- __User Profiles:__ Customizable profiles with profile picture, bios and posts.
  - Users can delete their profiles.
- __User Interaction:__ Follow and unfollow functionality.
  - Only authorized users are permitted to follow or unfollow users.
  - All users can view the list of followers or followings.
- __User Search:__ Search for users by username or full name.
- __Content Sharing:__ Interface for viewing, creating, updating, or deleting posts.
  - Post previews are displayed on author's profile in order from newest to oldest.
- __Content Interaction:__ Like and dislike feature for posts to enhance user engagement.
  - Only authorized users are permitted to like or dislike posts.
  - All users can view the list of users who liked a post.
- __News:__  News feed displays posts for all users with infinite scrolling.
- __Device Compatibility:__ Compatible with various devices to ensure a smooth user experience.
  - Web platform with responsive design which adapts the layout and content to various screen sizes.
- __Responsive design:__ Adaptive user interfaces that adjust seamlessly from smartphone to laptop screen sizes.
  - The UI adapts on smartphone views for screens with widths ranging from 320px (20rem) to 448px (28rem).
  - The UI adapts on laptop views for screens wider than 448px (28rem).
- __Security:__
  - Authentication is implemented using OAuth 2.0 ( Firebase Authentication ).
  - Strict validation for user inputs and data integrity.
  - Custom exception handler for error identification and debugging.

## AWS Setup

1. __IAM Setup:__
    - Create user with `AmazonS3FullAccess` permission.
    - Create access key in user security credentials save `Access key` and `Secret access key` for the future process.

2. __S3 Setup:__  
    - Create `profiles` and `posts` buckets.

## Firebase Setup

1. [Log in to Firebase](https://firebase.google.com/codelabs/firebase-nextjs#1)
2. [Create a Firebase project](https://firebase.google.com/codelabs/firebase-nextjs#2)
3. [Add a web app to your Firebase project](https://firebase.google.com/codelabs/firebase-nextjs#2)

## Environment Setup

1. Install Visual Studio Code (`ms-vscode-remote.remote-containers` extension)
2. [Install Docker Engine on Ubuntu](https://docs.docker.com/engine/install/ubuntu/#install-using-the-repository) and follow the [Linux post-installation steps for Docker Engine](https://docs.docker.com/engine/install/linux-postinstall/).
3. Clone the project repository with [Submodules](https://git-scm.com/book/en/v2/Git-Tools-Submodules).

    ```bash
    git clone --recurse-submodules https://github.com:Xamarsia/spsp-deployment.git
    ```

4. Docker network `microservice_network` required for further communication between the frontend and the backend.

    Execute the following command to create the network:

    ```bash
    docker network create microservice_network
    ```

5. [Setup environment for backend](https://github.com/Xamarsia/simple-photo-sharing-platform/tree/main#environment-setup).
6. [Setup environment for frontend](https://github.com/Xamarsia/photo-sharing-platform-frontend/tree/main#environment-setup).

## Build & Run

1. Open project in VS Code.

2. [Build & Run backend](https://github.com/Xamarsia/simple-photo-sharing-platform/tree/main#build--run).
3. [Build & Run frontend](https://github.com/Xamarsia/photo-sharing-platform-frontend/tree/main#build--run).

4. Open <http://localhost:3000> with your browser to see the result.

## UI Prototype

Only a few pictures are presented here. The others can be found in the [frontend repository](https://github.com/Xamarsia/photo-sharing-platform-frontend/tree/main#ui-prototype).

This UI has been designed in Figma prior to development.

Although some adjustments were made during the final development stages, the prototype still retains its core functionality and visual design.

### UI Prototype V 1.0 Smartphone

This initial prototype was created on a smartphone without any special styles, focusing primarily on the consistency of the components and the layout of the pages.

[SPSP Prototype V 1.0 Smartphone](https://www.figma.com/design/bgJwULPNm1froxp0PCcRLS/SPSP-Prototype-1.0?node-id=0-1&t=kYQT0MoLztvZ8u6X-1)

<p align="center">
  <img alt="SignIn" width="24%" src="https://github.com/user-attachments/assets/0ba6abe7-1e91-43d6-90c4-f245e2c8bec8" />
  <img alt="SignIn" width="24%" src="https://github.com/user-attachments/assets/4ae31493-8985-49da-8aa8-895f748a79aa" />
  <img alt="SignIn" width="24%" src="https://github.com/user-attachments/assets/2b9b7467-514a-41cd-9ac5-60741c16b983" />
  <img alt="SignIn" width="24%" src="https://github.com/user-attachments/assets/1eb3d9ab-13c1-49af-87dc-21e0230979ed" />
</p>

### UI Prototype V 1.0 PC

The second prototype was made to focus on styles and layouts.

[SPSP Prototype V 1.0 PC](https://www.figma.com/design/bgJwULPNm1froxp0PCcRLS/SPSP-Prototype-1.0?node-id=7601-347&t=kYQT0MoLztvZ8u6X-1)

<p align="center">
  <img alt="SignIn" width="32%" src="https://github.com/user-attachments/assets/5304f46c-1773-4673-93c1-2654f4eca187" />
  <img alt="SignIn" width="32%" src="https://github.com/user-attachments/assets/e1bc8d6b-1e58-4ad2-86fd-1bdc9cd11eee" />
  <img alt="SignIn" width="32%" src="https://github.com/user-attachments/assets/3e2f80fd-f329-4886-8448-114ef69aa49a" />
</p>

## Screenshots

Only a few pictures are presented here. The others can be found in the [frontend repository](https://github.com/Xamarsia/photo-sharing-platform-frontend/tree/main#screenshots).

### Desktop

<p align="center">
 <img alt="News" width="32%" src="https://github.com/user-attachments/assets/2573bf9a-ad2d-4926-af4d-7d8e31d5b5e1" />
 <img alt="Profile" width="32%" src="https://github.com/user-attachments/assets/b10dbd00-fa57-438c-b513-8129e9359097" />
 <img alt="Settings" width="32%" src="https://github.com/user-attachments/assets/4f81634e-ca56-454c-b7ed-281386323182" />
</p>

### Mobile

<p align="center">
  <img alt="Profile 01" width="24%" src="https://github.com/user-attachments/assets/98bcc6e7-f957-421a-9401-719afd61b703" />
  <img alt="Settings" width="24%" src="https://github.com/user-attachments/assets/04d37530-3517-401b-8170-c167da4b409a" />
  <img alt="Followings" width="24%" src="https://github.com/user-attachments/assets/fe77d928-523f-4579-9147-cc8da607200f" />
  <img alt="Post 01" width="24%" src="https://github.com/user-attachments/assets/e729564f-5d8a-42b6-a4fd-0aca8000634d" />

</p>

## Future Enhancements

- [ ] Utilize Nginx Ingress Controller as a reverse proxy and load balancer.
- [ ] Utilize `slf4j` logging.
- [ ] Add functionality for comments and hashtags.
- [ ] Increase test coverage.

## License

Licensed under the MIT License. See [LICENSE](./LICENSE) file for more details.
