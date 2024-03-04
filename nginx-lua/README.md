Nginx server with lua module enabled

Lua module will help us to expose more metrics to monitor nginx server


## Usage

- Build image: docker build . -t nginx-lua
- Execute: docker run -d -p 9145:9145 nginx-lua
- Test: curl localhost:9145/metrics 