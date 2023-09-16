# flutter-web-dockerfile
A demo how to setup flutter web in docker container. The demo code is from flutter official cookbook [Animate the properties of a container](https://flutter.dev/docs/cookbook/animation/animated-container). And the docker build web was learned and reference from [building a flutter web container](https://kevinwilliams.dev/blog/building-a-flutter-web-container).

# Command
## Build the docker image
Use docker build the container image
```
docker build -t myanimate-web .
```
If you have some problem during cache, you can clean cache by this
```
docker build --no-cache -t myanimate-web .
```

## After Success building image
Run the docker image with localhost 1200 port. You can change to any other port just replace it.
```
docker run -d -p 1200:80 --name myanimate myanimate-web
```

Here we go, open browser and go to http://localhost:1200/

# About the Dockerfile
In the Dockerfile line 15 checkout flutter specific version 3.13.0, and in a future we can continuous maintain and upgrade to the latest / stable or any desired version.