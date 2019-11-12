# heroku-docker-r-example-app

## Running this app locally using RStudio
Running this app with RStudio requires no additional changes. You can use RStudio to instal the libray dependencies for this app.
This application was built using R 3.6.1.

## Running this app locally using Docker
* Install Docker for your operating system
  - [Mac](https://docs.docker.com/docker-for-mac/install/)
  - [Windows](https://docs.docker.com/docker-for-windows/install/)
* Build the container
```docker build . -t heroku-docker-r-example-app```
* Run the container
```docker run -e PORT=8080 -p 8080:8080 heroku-docker-r-example-app```
* View the app locally in your web browser at <http://localhost:8080>

## Deploying this application to Heroku
1. ```heroku create --stack=container my-docker-r-example-app --team=g-harvard``` [1]
2. ```heroku git:remote -a my-docker-r-example-app```
3. ```git push origin heroku```
4. Visit the app - the app's url will be different based on what you've named it, but follows this template: <https://APPNAME.herokuapp.com>. For a working example, see <https://docker-r-example-app.herokuapp.com/>
[1] Replace ```my-docker-r-example-app`` with whatever name. ```---team``` is not necessary or non-IQSS/HMDC users.

