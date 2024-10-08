<h2 align=center>Upgrade Chasm Scout to v0.0.5</h2>

- First, stop the running Scout container to prepare for the update
```bash
docker stop scout
```
- Remove the old Scout container to avoid conflicts with the new version
```bash
docker rm scout
```

- Fetch the latest version of the Scout image from Docker Hub
```bash
docker pull chasmtech/chasm-scout:latest
```
- Start the Scout container with the updated images
```bash
docker run -d --restart=always --env-file ./.env -p 3001:3001 --name scout chasmtech/chasm-scout
```
- View the container logs to ensure there are no errors
```bash
docker logs scout
```
- Now, Test your server response, if everything is perfect you will get `OK` msg on terminal
```bash
curl localhost:3001
```
---
- Visit [this site](https://scout.chasm.net/dashboard)
- Connect wallet
- You will see v0.0.5 in the corner
