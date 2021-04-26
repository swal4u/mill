# README

Your shiny new Scala build tool! Confused by SBT? Frustrated by Maven? Perplexed by Gradle? Give Mill a try!

This dockerfile use the current user instead of default root user.

## How to use Dockerfile

Build the image

```code
docker build -t myimage \
  --build-arg USER_ID=$(id -u) \
  --build-arg GROUP_ID=$(id -g) .
```

Add alias in .bash_aliases

`alias mill='docker run --rm -it -e TZ=Europe/Paris -v $PWD:/app -w /app --name mill swal4u/mill'`

Start mill in your scala app folder

`mill`

## Sources

[Mill](https://github.com/com-lihaoyi/mill)

[docker shared permissions](https://vsupalov.com/docker-shared-permissions/)