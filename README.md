# storm_exporter

## How to run
Before run docker container should remember review in .env to be correct config

Copy ENV file 
```cmd
touch .env
cp sample.env .env
```

Build image
```commandline
docker build -t mr4x2/stormexporter:v1.2.2 . 
```

Run container with env
```commandline
docker run -d -p 8082:8082 --env-file .env --name stormexporter stormexporter
```

Or if you dont want to build dokcer image

```commandline
docker run -d -p 8082:8082 --env-file .env --name stormexporter mr4x2/stormexporter:v1.2.2
```