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


$ docker ps
CONTAINER ID   IMAGE          COMMAND                  CREATED       STATUS       PORTS                    NAMES
9f6a467242d3   10154fc3fe6a   "python manage.py ru…"   2 hours ago   Up 2 hours   0.0.0.0:8000->8000/tcp   lucid_ramanujan
df003ab3d167   10154fc3fe6a   "python manage.py ru…"   2 hours ago   Up 2 hours   0.0.0.0:8080->8080/tcp   ecstatic_robinson

$ docker stop 9f6a467242d3
9f6a467242d3
$ docker rm 9f6a467242d3
9f6a467242d3

$ docker logs df003ab3d167
Watching for file changes with StatReloader
System check identified some issues:

WARNINGS:
todos.Todo: (models.W042) Auto-created primary key used when not defining a primary key type, by default 'django.db.models.AutoField'.
        HINT: Configure the DEFAULT_AUTO_FIELD setting or the TodosConfig.default_auto_field attribute to point to a subclass of AutoField, e.g. 'django.db.models.BigAutoField'.

System check identified 1 issue (0 silenced).
$ docker inspect df003ab3d167
[
    {
        "Id": "df003ab3d167217e2a6f339a879fc0835a72ec0a9d0560f1dc077842f3f63fe5",
        "Created": "2023-11-02T08:06:17.8132084Z",
        "Path": "python",
        "Args": [
            "manage.py",
            "runserver",
            "0.0.0.0:8000"
        ],
        "State": {
            "Status": "running",
            "Running": true,
            "Paused": false,
            "Restarting": false,
            "OOMKilled": false,
            "Dead": false,
            "Pid": 1031,
            "ExitCode": 0,
            "Error": "",
            "StartedAt": "2023-11-02T08:06:18.227239Z",
            "FinishedAt": "0001-01-01T00:00:00Z"
        },
        "Image": "sha256:10154fc3fe6a19736a978ae36284ccc39d770b3d1cc3ad089890e51129128953",
        "ResolvConfPath": "/var/lib/docker/containers/df003ab3d167217e2a6f339a879fc0835a72ec0a9d0560f1dc077842f3f63fe5/resolv.conf",
        "HostnamePath": "/var/lib/docker/containers/df003ab3d167217e2a6f339a879fc0835a72ec0a9d0560f1dc077842f3f63fe5/hostname",
        "HostsPath": "/var/lib/docker/containers/df003ab3d167217e2a6f339a879fc0835a72ec0a9d0560f1dc077842f3f63fe5/hosts",
        "LogPath": "/var/lib/docker/containers/df003ab3d167217e2a6f339a879fc0835a72ec0a9d0560f1dc077842f3f63fe5/df003ab3d167217e2a6f339a879fc0835a72ec0a9d0560f1dc077842f3f63fe5-json.log",
        "Name": "/ecstatic_robinson",
        "RestartCount": 0,
        "Driver": "overlay2",
        "Platform": "linux",
        "MountLabel": "",
        "ProcessLabel": "",
        "AppArmorProfile": "",
        "ExecIDs": null,
        "HostConfig": {
            "Binds": null,
            "ContainerIDFile": "",
            "LogConfig": {
                "Type": "json-file",
                "Config": {}
            },
            "NetworkMode": "default",
            "PortBindings": {
                "8080/tcp": [
                    {
                        "HostIp": "",
                        "HostPort": "8080"
                    }
                ]
            },
            "RestartPolicy": {
                "Name": "no",
                "MaximumRetryCount": 0
            },
            "AutoRemove": false,
            "VolumeDriver": "",
            "VolumesFrom": null,
            "ConsoleSize": [
                0,
                0
            ],
            "CapAdd": null,
            "CapDrop": null,
            "CgroupnsMode": "host",
            "Dns": [],
            "DnsOptions": [],
            "DnsSearch": [],
            "ExtraHosts": null,
            "GroupAdd": null,
            "IpcMode": "private",
            "Cgroup": "",
            "Links": null,
            "OomScoreAdj": 0,
            "PidMode": "",
            "Privileged": false,
            "PublishAllPorts": false,
            "ReadonlyRootfs": false,
            "SecurityOpt": null,
            "UTSMode": "",
            "UsernsMode": "",
            "ShmSize": 67108864,
            "Runtime": "runc",
            "Isolation": "",
            "CpuShares": 0,
            "Memory": 0,
            "NanoCpus": 0,
            "CgroupParent": "",
            "BlkioWeight": 0,
            "BlkioWeightDevice": [],
            "BlkioDeviceReadBps": [],
            "BlkioDeviceWriteBps": [],
            "BlkioDeviceReadIOps": [],
            "BlkioDeviceWriteIOps": [],
            "CpuPeriod": 0,
            "CpuQuota": 0,
            "CpuRealtimePeriod": 0,
            "CpuRealtimeRuntime": 0,
            "CpusetCpus": "",
            "CpusetMems": "",
            "Devices": [],
            "DeviceCgroupRules": null,
            "DeviceRequests": null,
            "MemoryReservation": 0,
            "MemorySwap": 0,
            "MemorySwappiness": null,
            "OomKillDisable": false,
            "PidsLimit": null,
            "Ulimits": null,
            "CpuCount": 0,
            "CpuPercent": 0,
            "IOMaximumIOps": 0,
            "IOMaximumBandwidth": 0,
            "MaskedPaths": [
                "/proc/asound",
                "/proc/acpi",
                "/proc/kcore",
                "/proc/keys",
                "/proc/latency_stats",
                "/proc/timer_list",
                "/proc/timer_stats",
                "/proc/sched_debug",
                "/proc/scsi",
                "/sys/firmware"
            ],
            "ReadonlyPaths": [
                "/proc/bus",
                "/proc/fs",
                "/proc/irq",
                "/proc/sys",
                "/proc/sysrq-trigger"
            ]
        },
        "GraphDriver": {
            "Data": {
                "LowerDir": "/var/lib/docker/overlay2/bc8e5e394d4647203570397c3369fe2fa2094ff2715d5e87cd72c9c1b221b0dc-init/diff:/var/lib/docker/overlay2/o2mfq004ppd3bruwhgcqnnd7z/diff:/var/lib/docker/overlay2/lvf58vj9ahpj3ba0orm50xyym/diff:/var/lib/docker/overlay2/t0ktxhcohtpay0f2mca0j6qg3/diff:/var/lib/docker/overlay2/a1831e8285f39a141d2c585ef2f90df54f83240ec9d8e6f0b53944ac9dc396ee/diff:/var/lib/docker/overlay2/607cc1b278997bcb6753773f1f4e19de7bcdf8b491d2524df604b6b08905dd89/diff:/var/lib/docker/overlay2/5bc891e0533970891c67100f9c27dd79a5c148498751ca337eb0b447ca8d658a/diff:/var/lib/docker/overlay2/11f9890d9b2239171cf6c9c13f9cdf5bae98611e841e70f85ea80be77b8e4b33/diff:/var/lib/docker/overlay2/4fc975b9595ab8fd0983ef98624f9d51dfa780f9b615c68e1b11bf31e0376b08/diff:/var/lib/docker/overlay2/2a0ef3aabce2f476c2290ba87886715ce38a185e491c0e5bb98aedb80faa9672/diff:/var/lib/docker/overlay2/a9c02cf477564fb9a6725ff0c53a4539dbdb2bdacda9c2d0cab7a7edfabd01c6/diff:/var/lib/docker/overlay2/abde457a3006fb96ee8c05128c07c9e63bbc742f161fd7e6dbb32e03de5f657e/diff",
                "MergedDir": "/var/lib/docker/overlay2/bc8e5e394d4647203570397c3369fe2fa2094ff2715d5e87cd72c9c1b221b0dc/merged",
                "UpperDir": "/var/lib/docker/overlay2/bc8e5e394d4647203570397c3369fe2fa2094ff2715d5e87cd72c9c1b221b0dc/diff",
                "WorkDir": "/var/lib/docker/overlay2/bc8e5e394d4647203570397c3369fe2fa2094ff2715d5e87cd72c9c1b221b0dc/work"
            },
            "Name": "overlay2"
        },
        "Mounts": [],
        "Config": {
            "Hostname": "df003ab3d167",
            "Domainname": "",
            "User": "",
            "AttachStdin": false,
            "AttachStdout": true,
            "AttachStderr": true,
            "ExposedPorts": {
                "8080/tcp": {}
            },
            "Tty": false,
            "OpenStdin": false,
            "StdinOnce": false,
            "Env": [
                "PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin",
                "LANG=C.UTF-8",
                "GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305",
                "PYTHON_VERSION=3.12.0",
                "PYTHON_PIP_VERSION=23.2.1",
                "PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/c6add47b0abf67511cdfb4734771cbab403af062/public/get-pip.py",
                "PYTHON_GET_PIP_SHA256=22b849a10f86f5ddf7ce148ca2a31214504ee6c83ef626840fde6e5dcd809d11"
            ],
            "Cmd": [
                "python",
                "manage.py",
                "runserver",
                "0.0.0.0:8000"
            ],
            "Image": "10154fc3fe6a",
            "Volumes": null,
            "WorkingDir": "",
            "Entrypoint": null,
            "OnBuild": null,
            "Labels": {}
        },
        "NetworkSettings": {
            "Bridge": "",
            "SandboxID": "6f818c34dd50a50cc17f463a5a47884a950fe3b0758eb20764cdfd39359ba755",
            "HairpinMode": false,
            "LinkLocalIPv6Address": "",
            "LinkLocalIPv6PrefixLen": 0,
            "Ports": {
                "8080/tcp": [
                    {
                        "HostIp": "0.0.0.0",
                        "HostPort": "8080"
                    }
                ]
            },
            "SandboxKey": "/var/run/docker/netns/6f818c34dd50",
            "SecondaryIPAddresses": null,
            "SecondaryIPv6Addresses": null,
            "EndpointID": "dc787f4e48e674970e69eb3b1539f7008f6debe1d7fbd25267cf13e1bae9ead5",
            "Gateway": "172.17.0.1",
            "GlobalIPv6Address": "",
            "GlobalIPv6PrefixLen": 0,
            "IPAddress": "172.17.0.2",
            "IPPrefixLen": 16,
            "IPv6Gateway": "",
            "MacAddress": "02:42:ac:11:00:02",
            "Networks": {
                "bridge": {
                    "IPAMConfig": null,
                    "Links": null,
                    "Aliases": null,
                    "NetworkID": "690f3049cee7f4351aaf7d122219466e2980c27c687a798bc80b10ecca8ff944",
                    "EndpointID": "dc787f4e48e674970e69eb3b1539f7008f6debe1d7fbd25267cf13e1bae9ead5",
                    "Gateway": "172.17.0.1",
                    "IPAddress": "172.17.0.2",
                    "IPPrefixLen": 16,
                    "IPv6Gateway": "",
                    "GlobalIPv6Address": "",
                    "GlobalIPv6PrefixLen": 0,
                    "MacAddress": "02:42:ac:11:00:02",
                    "DriverOpts": null
                }
            }
        }
    }
]

$ docker exec -t df003ab3d167
"docker exec" requires at least 2 arguments.
See 'docker exec --help'.

Usage:  docker exec [OPTIONS] CONTAINER COMMAND [ARG...]

Execute a command in a running container
$ docker attach df003ab3d167
no result

df003ab3d167   ecstatic_robinson   0.00%     0B / 0B             0.00%     0B / 0B   0B / 0B     0
CONTAINER ID   NAME                CPU %     MEM USAGE / LIMIT   MEM %     NET I/O   BLOCK I/O   PIDS
df003ab3d167   ecstatic_robinson   0.00%     0B / 0B             0.00%     0B / 0B   0B / 0B     0


$ docker container restart df003ab3d167
df003ab3d167

$ docker top df003ab3d167
UID                 PID                 PPID                C                   STIME               TTY                 TIME                CMD
root                8892                8871                0                   10:50               ?                   00:00:00            python manage.py runserver 0.0.0.0:8000
root                8915                8892                1                   10:50               ?                   00:00:01            /usr/local/bin/python manage.py runserver 0.0.0.0:8000

$ docker start df003ab3d167
df003ab3d167

docker pause df003ab3d167
$ docker ps -a
CONTAINER ID   IMAGE          COMMAND                  CREATED       STATUS                  PORTS                    NAMES
df003ab3d167   10154fc3fe6a   "python manage.py ru…"   3 hours ago   Up 2 minutes (Paused)   0.0.0.0:8080->8080/tcp   ecstatic_robinson



Waqas.Rasheed@PK-WAQRASHE MINGW64 /d/Waqas/Assign01 (master)
$ docker unpause df003ab3d167
df003ab3d167

Waqas.Rasheed@PK-WAQRASHE MINGW64 /d/Waqas/Assign01 (master)
$ docker ps -a
CONTAINER ID   IMAGE          COMMAND                  CREATED       STATUS         PORTS                    NAMES
df003ab3d167   10154fc3fe6a   "python manage.py ru…"   3 hours ago   Up 3 minutes   0.0.0.0:8080->8080/tcp   ecstatic_robinson

Waqas.Rasheed@PK-WAQRASHE MINGW64 /d/Waqas/Assign01 (master)
$ docker port df003ab3d167
8080/tcp -> 0.0.0.0:8080

$ docker update df003ab3d167
you must provide one or more flags when using this command

