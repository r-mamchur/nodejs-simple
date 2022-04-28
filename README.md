# Node.js-simple
    
For test CI.

## TeamCity

## Drone.io
Branch '**dev**' is auto deployed into Development env.
Branch '**master**' is auto deployed into Test env.
Deployment into Production env. via the use of the promotion feature.
```
docker run \
--env=DRONE_SERVER=http://192.168.56.223:3022 \
--env=DRONE_TOKEN=<your token> \
drone/cli build promote r-mamchur/nodejs-simple <build number> production
```
or    
```
curl -i -v -X \
POST "http://192.168.56.223:3022/api/repos/r-mamchur/nodejs-simple/builds/<build number>/promote?target=product" \
-H "Authorization: Bearer <your token>"
```
