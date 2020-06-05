# docker-local-registry
This repository is used to create a local docker registry. It's integrated with basic authentication which makes it secure.

## Setting up authentication
1. Add a file under auth folder and name it registry.password
2. Add username and passoword into the registry.password file

To add a username and password, using command
```htpasswd registry.password username```
password will be asked after the command is executed.

## Starting up the project
Start up the local docker registry using command
```docker-compose up```

## Acessing the images on the browser
After starting up the local docker registry container, you can navigate to http://localhost:5000/v2/_catalog. The browser will ask for username and password. After you are authenticated, if no images are pushed, you will see something like this `{"repositories":[]}` on your browser.

