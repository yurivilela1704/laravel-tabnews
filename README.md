# Laravel TabNews

This repository documents my journey through curso.dev, where I’m building a clone of TabNews using Next.js and React. In parallel, I’m creating this project on my own, using Laravel, Vite, Inertia, and Vue.js. This dual approach allows me to learn full-stack development from both the JavaScript and PHP ecosystems, comparing workflows and best practices along the way.

This project is a Laravel-based application using Vite and Tailwind CSS for the frontend setup. Follow the steps below to set up and run the project.

---

## Commands
With Docker installed and the container up, run the following commands to get started:

### Build Frontend Assets
To build the frontend assets for production, use the following command: ``bash docker compose run --rm node npm run build``


This will generate the necessary CSS and JS files in the `public/build` directory.

---

### Development Server
To run Vite and enable hot module reloading for local development, use: ``bash docker compose run --rm --service-ports node npm run dev
``


Ensure you visit [http://localhost:8000](http://localhost:8000) after starting all containers to view the application.

---
