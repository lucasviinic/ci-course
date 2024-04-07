# Continuous Integration: Automated Tests and Pipeline on Github Actions

### Lesson 1: Understanding CI

- Understand the prerequisites needed to run the application, in our case Docker and Go, with Docker for our database and Go for managing the application;
- Set up the application's database using docker-compose, automating part of the task instead of having to manually remember and execute Docker's default command;
- Address an issue encountered in the docker-compose file related to volume configurations, ensuring proper file storage and enabling the execution of the database.

### Lesson 2: Testing Application

- Run automated tests for Go, and through this, verify if there are any logic issues in the application to be corrected;
- Execute tests verbosely, so that it's possible to see all tests being executed and how they are being executed. This way we can determine if any of them returned an error;
- Access GitHub Actions, so that we can start creating continuous integration routines;
- Create your first CI routine, using the suggested routine by Actions, and thus allow only a few lines to be changed.

### Lesson 3: Customizing routine

- What are the main fields of the jobs, having `runs-on` to choose the system, `steps` in conjunction with `run` to execute code, and `name` to name each step.
- How to execute code within the CI routine, so that we can prepare the environment and run the application tests, ensuring its logic.
- Starting a Docker container using `docker-compose up` within a pipeline, thus facilitating the environment setup.

### Lesson 4: Second Routine

- Change the execution order of commands within each job, making them faster, as in the case of tests and compilation, where it is not necessary to spend time compiling if the tests fail;
- Create a second job, which allows better separation of each function within the routine, facilitating the identification of problems and long-term maintenance;
- View routines in Github Actions, and check if any errors occurred and access the execution logs;
- Force an error, thus understanding what happens if this is encountered in the application and how this error is displayed for those who access the repository.

### Lesson 5: Utilizing strategies

- Working with matrix strategies enables the creation of various different development environments with minimal code, making the routine more organized.
- Creating and utilizing variables, such as go_version within the matrix strategy, allows for storing multiple values for later use.
- Utilizing secrets and thus creating an environment by placing a secret within it enables its use within the routine without sharing its value.
