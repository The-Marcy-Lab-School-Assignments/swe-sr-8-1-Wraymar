# swe-sr-8-1

For guidance on setting up and submitting this assignment, refer to the Marcy lab School Docs How-To guide for [Working with Short Response and Coding Assignments](https://marcylabschool.gitbook.io/marcy-lab-school-docs/fullstack-curriculum/how-tos/working-with-assignments#how-to-work-on-assignments).

## Prompt

![Fullstack Diagram](./client-server-database-diagram.svg)

You’ve been given a diagram (see above) showing the three core layers of a fullstack application:

- Frontend – a React application that users interact with
- Backend – an Express server that handles logic and communication
- Database – a PostgreSQL database that stores persistent data

Imagine you’re explaining how these layers work together by using a real-world example: Instagram.

Your task:

1. Explain how Instagram works using the three-layer diagram.

   - What happens when a user opens the app, scrolls through their feed, likes a post, or uploads a new photo?
   - Walk through how data flows from the frontend to the backend and to the database—and back again.

2. Come up with an analogy to help someone new to coding understand these layers.

- You might compare the system to something like a restaurant, a library, or even a post office—anything that helps make the roles of each layer intuitive.
- Make sure your analogy maps clearly to the roles of the frontend, backend, and database.

3. Reflect on the value of this separation.

- Why do we separate concerns into these layers?
- What would go wrong if we tried to do everything in one layer?

Audience: Imagine you're writing this for someone who's just starting out in web development and wants to understand how modern apps work.

Length: Around 400–600 words.

# Response

## How it all works together

When a user opens the app, scrolls through the feed, likes a post, or uploads a new photo, they are interacting with the user interface. This interface is designed to be simple and easy to understand, especially for someone who doesn't know any coding. This part of the application is called the **frontend**. When a user likes a post or uploads a photo, that data is processed and sent via an HTTP request to the **backend** (or server). The server handles the request and formats it in a way that allows it to be saved in the **database**. Later on, when another user tries to view that same photo, the data is pulled from the database, flows through the server, and is returned to the frontend so the image can be displayed.

## An Analogy to Understand

Imagine a coffee shop. A customer can walk in and order a coffee without ever needing to understand what happens behind the counter to make it. That’s basically the frontend—it’s meant to provide a smooth, straightforward experience that lets the client get what they want. In technical terms, placing your order is like making an HTTP request to the server (which would be the waiter or waitress). That server then “serves” the appropriate item ordered, whether it’s an iced latte, mocha, or just a plain black coffee.

But before that coffee shows up, some behind-the-scenes magic happens. The order leaves the server and enters the database through a specific query based on what was requested. Think of it like the waitress writing your order ticket and sending it to the backroom to get the right ingredients. Finally, the data (ingredients) comes out of the database, is prepared by the server (the waitress mixing your drink), and is delivered back to the client through the frontend (the waiting area).

## Why we separate these layers

We do this for a few key reasons. First, **separation of concerns**—a core principle in web development—means keeping different types of code in their own respective places. This makes everything easier to read and maintain and makes fixing bugs much simpler.

Beyond readability, some parts of an application simply have to be separate or they wouldn’t function correctly. We also don’t want users seeing everything that’s going on under the hood. Imagine driving a see-through car and watching the drive shaft spin, the pistons fire, and the engine combust—pretty unsettling, unless you’re a hardcore car enthusiast. The same goes for software: some things are best kept behind the scenes.
