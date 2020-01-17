# How To Run

run command: 

```s
docker run -p ${YOUR_PORT}:80 -p 5900:5900 -e VNC_PASSWORD=${YOUR_PASSWORD} -v /dev/shm:/dev/shm gnawfortune/ucore_env
```

- `${YOUR_PORT}`: Port for accessing desktop through browser
- `${YOU_PASSWORD}`: Password for accessing the desktop.

Then, you can access the desktop through the browser using the port you set.