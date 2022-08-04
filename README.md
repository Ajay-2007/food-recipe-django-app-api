# food-recipe-django-app-api
Recipe API project.


### Deployment commands

#### start the app in background
```bash
docker-compose -f docker-compose-deploy.yml up -d
```

### After making the changes to the services
- first we build the app
```bash
docker-compose -f docker-compose-deploy.yml build app
```
- start the only service which we made changes to such as `app` service


```bash
docker-compose -f docker-compose-deploy.yml up --no-deps -d app
```
--no-deps means don't restart the other dependency services which are defined in the docker-compose-deploy.yml file only restart the app service file