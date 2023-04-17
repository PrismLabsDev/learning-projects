# Learning Projects

Prisms Labs has put together this repository to help developers with project based learning. We maintain documentation outlining several different demo projects designed to explore a wide range of language and framework features. We also include a general docker configuration that will run PostgreSQL, MongoDB and Mailpit to aid in development. Each project contains detailed documentation including: overall project goals and scope, user stores, data relationships, api routes, pages, components and global state. We will also include a postman collection in each project so you can easily test the routes you build according to the documentation.

# Projects

## [Portfolio](https://github.com/PrismLabsDev/learning-projects/tree/main/projects/portfolio)

We will create a virtual resume / portfolio site to showcase ourselves and our work as we continue to learn. This is a front end only project and is a good project for learning a new JS UI framework, design system or implement in vanilla HTML and CSS if you are just starting out in web development.

## [Todo](https://github.com/PrismLabsDev/learning-projects/tree/main/projects/todo)

We will create a basic todo application that will alow users to perform CRUD operations on a list of TODO items. We will also create a basic dashboard that features a clock we program ourselves in JS and pull the current weather from an open and free API. This is a good project if you are just getting started in web development. The documentation for this project is broken into two stages, front end only where we store all our todo items in the browsers local storage and the second stage where we can optionally create an API to store the todo data and implement an authentication system.

## [Blog](https://github.com/PrismLabsDev/learning-projects/tree/main/projects/blog)

This is a full stack blog application which has similar features to [Medium](https://medium.com/) or [Dev.to](https://dev.to/). This is overall a well rounded project and a good option to choose if you are looking to explore web development more in depth, or if you are learning a new language or framework and want to explore its features. On the back end we will explore HTTP requests and data relationships in more complexity than in the Todo app. On the front end we will explore page routing, application state.

## [Chat](https://github.com/PrismLabsDev/learning-projects/tree/main/projects/chat)

This is a full stack chat application which takes advantage of web sockets to perform real time bidirectional communication. This project is simple on the server but introduces you to a new way to communicate fro client to server.

# Docker Environment

We have included a general docker environment to give you access to PostgreSQL, MongoDB and Mailpit. This allows you to build your projects with and SQL or NOSQL database, as well as test sending emails.

**All commands must be ran in the ```docker``` directory.**
``` bash
# Start environment
docker-compose up -d

# Stop docker environment
docker-compose down

# Reset data
rm -rf volumes
```

<div style="display: flex; flex-direction: row; column-gap: 30px; margin: 20px; 0px;">
  <div>
    <p style="text-align: center"><b>PostgreSQL</b></p>
    <table>
      <tr>
        <td>Host</td>
        <td>localhost</td>
      </tr>
      <tr>
        <td>Port</td>
        <td>5432</td>
      </tr>
      <tr>
        <td>Database</td>
        <td>general</td>
      </tr>
      <tr>
        <td>User</td>
        <td>user</td>
      </tr>
        <tr>
        <td>Password</td>
        <td>password</td>
      </tr>
    </table>
  </div>
  <div>
    <p style="text-align: center"><b>MongoDB</b></p>
    <table>
      <tr>
        <td>Host</td>
        <td>localhost</td>
      </tr>
      <tr>
        <td>Port</td>
        <td>27017</td>
      </tr>
      <tr>
        <td>User</td>
        <td>user</td>
      </tr>
        <tr>
        <td>Password</td>
        <td>password</td>
      </tr>
    </table>
  </div>
  <div>
    <p style="text-align: center"><b>Mailpit</b></p>
    <table>
      <tr>
        <td>Host</td>
        <td>localhost</td>
      </tr>
      <tr>
        <td>Port (SMTP)</td>
        <td>1025</td>
      </tr>
      <tr>
        <td>Port (Web UI)</td>
        <td>8025</td>
      </tr>
      <tr>
        <td>User</td>
        <td>NULL</td>
      </tr>
        <tr>
        <td>Password</td>
        <td>NULL</td>
      </tr>
    </table>
  </div>
</div>

# Recommended Tools / Technology

* [VS Code](https://code.visualstudio.com/)
* [Git](https://git-scm.com/)
* [Docker](https://www.docker.com/)
* [Postman](https://www.postman.com/)
* [DBeaver](https://dbeaver.io/)
* [Mongo Compass](https://www.mongodb.com/products/compass)
