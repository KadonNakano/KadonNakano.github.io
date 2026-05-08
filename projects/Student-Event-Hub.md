---
layout: project
type: project
image: img/MW/mwlogo.jpeg
title: "MW"
date: 2024
published: true
labels:
  - Final Project
summary: "An overview of my Final Project, a web application called Student Event Hub."
---

# Student Event Hub Web Application

Student Event Hub is a student-focused web application designed to make campus events easier to find, save, review, and manage. It solves the problem of students missing events or struggling to track them by providing a digitized event calendar where users can browse current and future SLD events, filter or search by categories and other criteria, add events to their own “Your Events” page, create new events, edit existing ones, and leave feedback through likes/dislikes. The project also includes admin features for managing events, making it a centralized hub for both students and organizers.

During the development of the project, I worked on several smaller tasks, including creating the starting points for pages such as the “All Events” and “Your Events” pages, as well as making small adjustments and bug fixes throughout the application. The features I had the most responsibility for were the like/dislike feature and the search bar. The like/dislike feature was more of a headache than we had anticipated because it required handling authentication, preventing unsigned users from voting, separating client-side UI logic from server-side database updates, updating vote counters correctly, and eventually adding permanent per-user vote tracking through the database. Through this process, I gained a much better understanding of how frontend state, server actions, Prisma, and database schema changes work together in a full-stack application.

<img src="/img/sehub.png" alt="Student Event Hub screenshot" width="80%">

[Link to Student Event Hub Organization Github Page](https://github.com/student-event-hub)
