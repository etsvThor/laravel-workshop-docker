# Laravel Workshop Docker install

This workshop uses a [Docker](https://www.docker.com/)-based environment, so that you can work on the project without you needing to install all the dependencies for Laravel in your host.
This also allows everyone in the workshop to have the same work environment, which helps with error resolving as well.

The system we use is based on [Laravel Sail](https://laravel.com/docs/9.x/sail).

## Installation

First install [Docker desktop](https://www.docker.com/products/docker-desktop/) (if you run Linux, just use your package manager to install the software!), and [Docker compose](https://docs.docker.com/compose/install/), if it was not isntalled with the desktop package.
Once this is installed successfully, try the command `docker info`. If it gives a lot of permission errors, you can give yourself access to the docker deamon by running the command `sudo usermod -aG docker <your_wsl_name>`. 

Now run the script `create_laravel_instance.sh` in a Bash shell (on Windows: open the [Windows Subsystem for Linux](https://docs.microsoft.com/en-us/windows/wsl/install) and navigate to this file):

```
$ ./create_laravel_instance.sh
```

Follow the instructions outputted by this script to start your system. Once you have launched the system, you can follow the rest of the workshop.

### Accessing the locally hosted website

You can access the locally hosted website by navigating to `localhost` in your browser.

#### Port is aready allocated

If the error "port is already allocated" comes up, you can change the port used by docker to any other port (it is commen to choose a port between 1024 and 65535) and store it in your `.env` file in the root of the laravel project:

laravel-workshop-blog/.env
```
[...]
APP_PORT=8081
[...]
```

## Docker

Think of docker like a virtual machine environment (technically it is a container based system, but that is up to you to research online), whichis commenly used in development environments to guarantee similar work environments and easy configuration of these work environments.
