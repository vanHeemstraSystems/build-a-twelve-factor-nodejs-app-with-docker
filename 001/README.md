# 001. Summary & Concepts of the Twelve-Factor App

See also [https://12factor.net](https://12factor.net)

Video: [https://egghead.io/lessons/egghead-summary-concepts-of-the-twelve-factor-app](https://egghead.io/lessons/egghead-summary-concepts-of-the-twelve-factor-app)

The twelve-factor app is a development and deployment methodology for building apps with present-day concepts. Following it will ensure your app can be deployed easily and scaled effortlessly.

The website 12factor.net explains the concepts of the twelve-factor app. The lessons in this course each directly relate to one of the 12 factors and are presented in order. The first few go over revision control and managing the config and dependencies of your Node.js app, while the rest explain the devops of your app with Nginx & Docker, with concepts closely aligned to the 12-factor app.

## The Twelve Factors

### I. Codebase
One codebase tracked in revision control, many deploys

### II. Dependencies
Explicitly declare and isolate dependencies

### III. Config
Store config in the environment

### IV. Backing services
Treat backing services as attached resources

### V. Build, release, run
Strictly separate build and run stages

### VI. Processes
Execute the app as one or more stateless processes

### VII. Port binding
Export services via port binding

### VIII. Concurrency
Scale out via the process model

### IX. Disposability
Maximize robustness with fast startup and graceful shutdown

### X. Dev/prod parity
Keep development, staging, and production as similar as possible

### XI. Logs
Treat logs as event streams

### XII. Admin processes
Run admin/management tasks as one-off processes
