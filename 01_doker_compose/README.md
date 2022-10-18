# Project assignment: Docker-compose

Let's get started with DevOps security. Configure the startup of all system components (Django, Nginx and Postgresql) with
docker-compose.

**Job Requirements:**

- Write a dockerfile for Django.
- To configure Nginx, you can use the developments from this topic, but the reviewers will definitely run your solution, so be sure
  that everything is working correctly.
- Remove Nginx version from headers. It is better to always hide versions of any software from prying eyes so that your admin panel is not accidentally hacked.
  View measurements in the official documentation and check that it works correctly. You can verify this with
  "Developer Tools" in the browser.
- Supports Django files via Nginx to avoid using fast service with extra requests: redefine `location` in such a way,
  to query for `/admin` went without looking for static accumulation. That is, bypassing the `try_files $uri $uri/ @backend;` directive.

**Tips and Tips:**

- This lesson should be enough to understand the configuration. If you have any questions about the parameters, look for
  answers [in the official documentation](https://nginx.org/ru/).
- To perform a task about `/admin`, you need to look at the search order for `location`.
- To work with static, you need to think about how to upload data to the file system of the container with Nginx.
- A basic structure is given for the task that can be used.

## Deploy

- We build the image and run the containers: `docker-compose up -d --build`
- Migrations will run themselves. Static files are collected by themselves.
- Create user: `docker-compose exec web python manage.py createsuperuser`
- Open the browser [admin panel] (http://127.0.0.1/admin/) (http://127.0.0.1/admin/)