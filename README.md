# OpenAI Whisper on Docker

## Build Docker Image

```shell
docker image build --tag whisper:latest .
```

## Run `whisper` Command

```shell
VOLUME_DIRECTORY=$(pwd)
FILE_NAME=hello.wav
docker container run --rm --volume ${VOLUME_DIRECTORY}:/data whisper --model small --language English /data/${FILE_NAME}
```

> Command Example on Windows: `docker container run --rm --volume C:/Users/USER_NAME/tmp:/data whisper --model small --language English /data/hello.wav`
