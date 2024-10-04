# Lib Postal REST Server

## Image

Use the docker image ```brandencolen/libpostal-rest:latest```

## Deploy

Use the ```.toml``` file in the project. The build section is the important bit

```
[build]
  image = 'brandencolen/libpostal-rest:latest'
```

Also not the extra RAM requirement

Use the following to deploy ```fly launch --name d4k-address --image brandencolen/libpostal-rest:latest```. That was used to build the ```.toml```file. That will deploy two machines, one can be destroyed using ```fly machine destroy <machine id> --force```. Also can use the ```--ha=false```to try and only deploy one machine.