# Democracy Kit Open EdX Devstack

This is the repository for getting set up with a local dev environment for working on Democracy Kit's Open EdX site.

## Installation Instructions

1. Install [docker-compose](https://docs.docker.com/compose/install/)
2. Make sure you have **make** and **pip** installed
4. Install [virtualenv](http://docs.python-guide.org/en/latest/dev/virtualenvs/#lower-level-virtualenv)
3. Clone this repository using:
  ```
  git clone https://github.com/democracykit/devstack.git
  ```
4. Move into the project folder and create a virtualenv using:
  ```
  virtualenv democracykit
  source democracykit/bin/activate
  ```
5. Then install requirements like so:
  ```
  make requirements
  ```
6. The Docker Compose file mounts a host volume for each service's executing code by conducting this command:
  ```
  make dev.clone
  ```
7. Run the provision command to configure the superusers (this may take a while):
  ```
  sudo make dev.provision
  ```
8. Start the services (this may take up to 60 seconds to appear):
  ```
  sudo make dev.up
  ```

And voila! You should have a version of Open EdX devstack running on your local machine. All of the services are running at the following links:

| Service             | URL                                 |
|---------------------|:------------------------------------:|
| Credentials         | http://localhost:18150/api/v2/      |
| Catalog/Discovery   | http://localhost:18381/api-docs/    |
| E-Commerce/Otto     | http://localhost:18130/dashboard/   |
| LMS                 | http://localhost:18000/             |
| Studio/CMS          | http://localhost:18010/             |

Once you're done with working for the day you can stop the services using:
```
make stop
```

## Further Help

If you want to see more detailed documentation navigate to the README in the /deprecated-files folder if you have any further questions.

 
