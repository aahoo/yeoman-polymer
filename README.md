# [yeoman + generator-polymer docker image](https://hub.docker.com/r/aahoo/yeoman-polymer/)

## Test Drive
1. run: `docker run -it --rm -p 5000:5000 aahoo/yeoman-polymer`
2. `yo polymer`
3. `gulp serve`
4. open browser > "virtual machine IP":5000 (e.g. http://192.168.99.100:5000/)

## Regular Use
Mount a host directory to the container

### Need to do only for the first run
1. `mkdir -p my-project && cd $_`
2. `docker run -it -p 5000:5000 -v $(pwd):/home/yeoman/my-project --name yo  aahoo/yeoman-polymer`
> In windows, you may have to change `$(pwd)` to `/$(pwd)`
3. `yo polymer`
4. `gulp serve`
5. open browser > "virtual machine IP":5000 (e.g. http://192.168.99.100:5000/)

### Need to do for the following runs
1. `cd PROJECT_FOLDER`
2. `docker start -i yo`
3. `gulp serve`
4. open browser > "virtual machine IP":5000 (e.g. http://192.168.99.100:5000/)
