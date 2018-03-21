#Democracy Kit Open EdX Devstack

This is the repository for getting set up with a local dev environment for working on Democracy Kit's Open EdX site.

##Installation Instructions

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
  ```
5. Then install requirements like so:
  ```
  make requirements
  ```
6. 
