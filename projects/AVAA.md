---
layout: project
type: project
image: img/projects/AVAA/AVAA_logo.png
title: "AVAA (Vaccination Helper Website)"
date: 2025-08-02
published: true
labels:
  - JavaScript
  - Fullstack Development
  - Node
  - MongoDB
  - Express
  - React
  - Redux
  - Bootstrap
summary: "AVAA is a straightforward full-stack app designed to simulate a website assistant that helps patients and medical staff schedule and manage vaccination appointments. It also provides simple data visualizations to report on appointment trends and patient demographics."
---
# AVAA - Assistant for Vaccination Appointments and Analytics
<figure class="figure w-20 float-end m-2">
    <img class="img-fluid" src="../img/projects/BC_AoU/aou_logo.png" alt="All of Us Program Logo">
</figure>

## Project Overview

AVAA (Assistant for Vaccination Appointments and Analytics) is a proof-of-concept application built with the MERN stack (MongoDB, Express, React, Node.js) to demonstrate a functional end-to-end system for managing vaccination appointments and analytics.

The backend is developed with Express.js, interfacing with a local MongoDB database to handle CRUD operations for user profiles, demographic data, appointment records, and vaccine/hospital listings. The frontend is built with React.js, leveraging reusable components and React-Bootstrap for responsive UI design.

Users can:
- Log in to their accounts.
- Browse available vaccines and hospitals.
- Request vaccination appointments.
- View their past and upcoming appointments.
- Pay for upcoming appointments.

Additionally, users with administrator privileges can create new vaccine listings and approve pending appointments. As a personal design-choice, records are unable to be deleted by patients or medical administrators.

Basic analytics, such as demographic distributions by gender, age, and profession, are publicly accessible to all visitors on the default landing page.

## Tech Stack

### Backend - Express API

The Express API techstack utilizes a number of modern Node packages to build a scalable backend API. The core framework is *Express.js* which handles HTTP requests and routing. *mongoose* is used for interacting with a local *Mongo DB* database. *dotenv* manages environment variables holding sensitive information, and *cors* ensures proper cross-origin resource sharing. For authentication, the app uses *jsonwebtoken* (JWT) for token-based authentication with a graceful 5 minute token-refresh period. User's passwords are hashed using *bcryptjs*. *faker* is used for generating random mock data for development and testing. *pdfmake* is used for generating certificate PDFs for vaccination appointments, and the *AWS-SDK S3* modules are used for interacting with the AWS environment and resources, which includes uploading PDFs and generating presigned URLs for users to download from the bucket directly.

### Frontend - React UI

The React UI techstack utilizes a number of modern UI-related packages to build a clean, navigable client-side user experience. The core framework is *React.js* and its related packages which allows for dynamic component-based UI, routing within React, single-paged applications (SPA), and integration with *Bootstrap* for styling. *redux* is used for state management across a user's site session. *axios* is used for Promise-based communication with the Express API. *d3* is used for dynamic data visualizations. *pdfmake* is used for generating certificate PDFs on client-side (particularly for appointments that have not yet been completed).

Webpack is used to compile and bundle JS, CSS, and other static assets into optimized files that are ready to be served to the browser. For styling, it uses *css-loader* to process CSS imports within JavaScript modules and *style-loader* to inject those styles dynamically into the HTML document at runtime. The *HTML Webpack Plugin* automates the injection of the generated JS and CSS bundles into the root HTML file. *Babel* serves as the JS transpiler, converting modern JS (ES6+ features) and JSX syntax into backwards-compatible ES5 code for a wider range of browser support.

## Future Steps

To expand on this project into a more fully-developed production style application, future steps could include:
- Integrate secure payment processing through a third-party payment gateway.
- Expand analytics capabilities with advanced visualizations and filtering options based on demographic data (age, gender, profession, etc.).
- Revamp the user interface (UI) with a modern, responsive design for improved user experience across devices.
- Email notification reminders about upcoming appointments.

## Links

View the [GitHub Repository](https://github.com/jeremiahdy55/VaccineDataHub-MERN).
