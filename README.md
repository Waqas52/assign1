# django-todo
A simple todo app built with django



```
You will need django to be installed in you computer to run this app. Head over to https://www.djangoproject.com/download/ for the download guide

Once you have downloaded django, go to the cloned repo directory and run the following command

```bash
$ python manage.py makemigrations
```

This will create all the migrations file (database migrations) required to run this App.

Now, to apply this migrations run the following command
```bash
$ python manage.py migrate
```

One last step and then our todo App will be live. We need to create an admin user to run this App. On the terminal, type the following command and provide username, password and email for the admin user
```bash
$ python manage.py createsuperuser
```

That was pretty simple, right? Now let's make the App live. We just need to start the server now and then we can start using our simple todo App. Start the server by following command

```bash
$ python manage.py runserver
```

git commands
$ git add -all
-- to add all changes from local to stage area
$ git commit -m "First commit"
-- ensure commit on stage area
$ git remote add origin https://github.com/Waqas52/assign1.git
add to remote repo

Faced error of remote origin already exit 
$git remove origin  removed oring

$ git push origin main https://github.com/Waqas52/assign1.git
--pushed code to remote repo

$docker version
installation of docker and version confirmation 
Client:
 Cloud integration: v1.0.35+desktop.5
 Version:           24.0.6
 API version:       1.43
 Go version:        go1.20.7
 Git commit:        ed223bc
 Built:             Mon Sep  4 12:32:48 2023
 OS/Arch:           windows/amd64
 Context:           default

Server: Docker Desktop 4.25.0 (126437)
 Engine:
  Version:          24.0.6
  API version:      1.43 (minimum version 1.12)
  Go version:       go1.20.7
  Git commit:       1a79695
  Built:            Mon Sep  4 12:32:16 2023
  OS/Arch:          linux/amd64
  Experimental:     false
 containerd:
  Version:          1.6.22
  GitCommit:        8165feabfdfe38c65b599c4993d227328c231fca
 runc:
  Version:          1.1.8
  GitCommit:        v1.1.8-0-g82f18fe
 docker-init:
  Version:          0.19.0
  GitCommit:        de40ad0

vi dockerfile. 
edited docker file with vi editor

$ docker build . -t todo-app
images creation from docker file 

$docker images
-- list of all images
$docker container ps -a 
list of all containers in docker

$ docker run -p 8000:8000 10154fc3fe6a
container created on port 8000 with image id 

$ winpty docker login 
 logged in docker hub
with regular docker login there was error of can not performinteractive login from non tty devide)


$ docker tag todo-app:latest waqas52/assign01
docker image placed to staging area( before placing it to docker hub)

$ docker push waqas52/assign01
pusher docker image to waqas52 username of repo assign01




