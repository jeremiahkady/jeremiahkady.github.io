---
layout: project
type: project
image: img/projects/SpringAIHotelChatbot/hotel.png
title: "Hotel Registry with AI-powered Chatbot"
date: 2025-07-04
published: true
labels:
  - Java
  - JavaScript
  - Fullstack Development
  - Spring-Boot
  - PostgreSQL
  - OpenAI
  - React
  - JWT (JSON web token)
  - React
summary: "This application is designed to simulate a hotel booking website that spans a multi-hotel network. It includes a built-in chatbot that understands and responds to user queries in natural language, powered by OpenAI's advanced NLP models."
---

## Project Overview

This project implements a microservice-based application that simulates the core functionality of a hotel booking website. Key features include:
 - Hotel Information & Booking Services
    - RESTful APIs for backend processing and data retrieval
    - React.js frontend for simple, component-based user interface
 - Secure Authentication
    - Stateless JWT-based authentication for users to access secured content
 - AI-powered Chatbot Integration
    - An NLP-driven conversational assistant embedded into the platform
    - Leverages basic OpenAI API calls on user queries combined with conversational and/or data context
 - Vector Similarity Search for Data Retrieval
    - Vector embeddings and vector similarity search for retrieving contextually relevant records from the database

## Project Architecture

The project is split into three different microservice applications:
 - [Frontend - React UI](#frontend---react-ui)
 - [Backend - Database Access](#backend---database-access)
 - [JWT Security & Authentication](#jwt-security--authentication)

### Frontend - React UI

<figure class="figure float-end mt-3 ms-2 mb-3">
    <img class="figure-img img-fluid" src="../img/projects/SpringAIHotelChatbot/react.png" style="height:200px;" alt="React.js Logo">
</figure>

The React UI microservice techstack uses *React.js* and its related packages to build a dynamic, component-based UI, enable routing within the single-paged applications (SPA), and integrated *Bootstrap* for styling. Webpack is used to compile and bundle JS, CSS, and other static assets into optimized files that are ready to be served to the browser. *Babel* serves as the JS transpiler, converting modern JS (ES6+ features) and JSX syntax into backwards-compatible ES5 code for a wider range of browser support. 

### Backend - Database Access

<figure class="figure float-start mt-3 me-2 mb-3">
    <img class="figure-img img-fluid" src="../img/projects/SpringAIHotelChatbot/postgresql.png" style="height:200px;" alt="PostgreSQL Logo">
</figure>

The backend microservice is built with Spring Boot and powered by *Spring Data JPA* for database interactions with a *PostgreSQL* instance enhanced by the *pgvector* extension for vector-based similarity search. It uses *Apache HTTP Client 5* to communicate with OpenAI’s APIs for both text responses and embedding generation. The generated embeddings are stored in the database and leveraged for semantic search (using vector cosine similarity), enabling the system to return relevant hotel or hotel-room data for natural language queries and responses. *Spring AI* helps streamline AI model integration, and *Jackson* is used for efficient JSON processing. This service is responsible for creating, retrieving, and managing all hotel, room, and booking records in the system.

### JWT Security & Authentication

<figure class="figure float-end mt-3 ms-2 mb-3">
    <img class="figure-img img-fluid" src="../img/projects/SpringAIHotelChatbot/jwt.png" style="height:200px;" alt="JWT Logo">
</figure>

The JWT Security microservice is built with Spring Boot and powered by *Spring Security* for authentication and authorization. It uses *Spring Data JPA* with a *PostgreSQL* database for secure and efficient data persistence, and *JJWT* (Java JWT) for JSON Web Token handling. This service acts as a gateway, blocking unauthorized access to database resources and ensuring that every request from the React UI passes through token verification. JWTs are issued and validated using RSA256 signing with public and private keys. When a user logs out, the issued token is added to a “revoked list,” preventing it from being reused.

## Key Takeaways & Future Steps

To expand on this project into a more fully-developed production style application, future steps could include:
- Conversation storage per user, allow user to view past chats (also clear stale chats)
- More robust multi-lingual support
   - Currently, user must prompt for a certain language first
- Greater hotel and hotel-room data variety to test the effectiveness of vector similarity search
- More robust data validation when submitting a booking request
- Integration with a banking/payment service

## Links

View the [Project Presentation](https://github.com/jeremiahdy55/springAIchatbot/blob/main/Hotel%20Chatbot%20Project%20-%20June%202025.pdf).

View the [GitHub Repository](https://github.com/jeremiahdy55/springAIchatbot).
