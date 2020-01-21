# ucore-env

Image for ucore os learning. The environment is set up based on official instruction.

## How To Run

run command: 

```shell
docker run --name ucore_env -d -p ${YOUR_PORT}:80 -p 5900:5900 -e VNC_PASSWORD=${YOUR_PASSWORD} -v /dev/shm:/dev/shm gnawfortune/ucore-env 
```

- `${YOUR_PORT}`: Port for accessing desktop through browser
- `${YOU_PASSWORD}`: Password for accessing the desktop.

This will create a container called `ucore_env` in background, then you can access the desktop through the browser using the port you set.

The code for ucore os lab is in `/root/code`.

To start/stop a container, use following commands:

```shell
docker start ucore_env # start
docker stop ucore_env # stop
```

## Tips

- You can use `-v` to make your own ucore os code on your machine mounted into a container. This ensures that your changes are not lost as the **container is removed** (start/stop is fine). See [This Link](https://docs.docker.com/storage/bind-mounts/) for more details.
  > `-v` or `--volume`: Consists of three fields, separated by colon characters (`:`). The fields must be in the correct order, and the meaning of each field is not immediately obvious.
  > - In the case of named volumes, the first field is the name of the volume, and is unique on a given host machine. For anonymous volumes, the first field is omitted.
  > - The second field is the path where the file or directory are mounted in the container.
  > - The third field is optional, and is a comma-separated list of options, such as `ro`. These options are discussed below.

- This image is based on `dorowu/ubuntu-desktop-lxde-vnc`, so you can see its [home page](https://hub.docker.com/r/dorowu/ubuntu-desktop-lxde-vnc) for more options.