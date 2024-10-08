# Project background and initial configuration

We are participating in the 2024 NASA Space Apps Challenge "Landsat Reflectance Data: On the Fly and at Your Fingertips" - with specific challenge details, requirements, and resources identified at [https://www.spaceappschallenge.org/nasa-space-apps-2024/challenges/landsat-reflectance-data-on-the-fly-and-at-your-fingertips/](https://www.spaceappschallenge.org/nasa-space-apps-2024/challenges/landsat-reflectance-data-on-the-fly-and-at-your-fingertips/) - although a copy of this exact information exists [here](../documentation/challenge_landsat_reflectance_data.md) for reference.

This project consists of a Next.js web application that can use Next.js route handlers (API routes) on the backend as well as Python code via a FastAPI backend.

The project [README](../README.md) contains important information about the project structure, initial setup and configuration, and notes about the deployed web application on Vercel.

There are a couple of important things to consider in terms of the web application:

- We are using Next.js v14 for a TypeScript React web application - which has its source code and assets contained within the `./app` directory
- Backend Next.js route handlers are defined as subdirectories of `./app/api` for all TypeScript and JavaScript code (`route.ts` or `route.js`, respectively)
  - To invoke our example `ping` endpoint, the front-end code would need to call the `/api/ping` endpoint
- A Python backend powered by FastAPI is contained in the `./api` directory
  - To invoke our example `ping` endpoint, the front-end code would need to call the `/api/py/ping` endpoint

As an experienced React and Python developer, you will be expected to suggest and enforce best practices for creating modular, reusable, and testable code.

Please make sure that for any Next.js changes you are making:

- Subdirectories for components, services, etc. should all be properly created underneath the `app` directory
- Backend Next.js API routes need to use the route handler example - which creates appropriate subdirectories for the endpoint with a `route.ts` file

Please make sure that for any Python FastAPI changes you are making:

- Best practices are followed for defining routes and the code they invoke
- Modules are refactored into the simplest form for ease of testing and development
- FastAPI `api/` routes must be `/api/py/` for this project

Please make sure that you include the complete path and filename of any code that you create or modify as a commented line at the top of the file for reference.
