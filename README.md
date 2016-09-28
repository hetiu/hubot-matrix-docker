# Hubot adapter for matrix

## Quick how-to

### Prerequisties

- Account created for the bot in a matrix server (login & password are required)
- Docker installed


### Deploy the bot

Build the bot Docker image.

```
git clone <this repo>
cd hubot-matrix-docker
docker built -t nic0d/hubot-matrix-docker .
```
 ... or download it from Docker Hub

```
git pull nic0d/hubot-matrix-docker
```

Execute the bot

```
docker run -it --rm -e HUBOT_MATRIX_PASSWORD=<bot-password> --e HUBOT_MATRIX_HOST_SERVER=<server-url> --name hubot-matrix -e BOT_NAME=<bot-name> nic0d/hubot-matrix
```
### Test the bot

- connect in the matrix Server with a regular user Account
- invite the bot in a room
- chat with the bot (<bot-name> help may helps)

Optional parameter:
 -e HUBOT_LOG_LEVEL=debug
