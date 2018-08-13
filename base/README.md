# Alpine Base with s6


This is base docker image based on alpine linux
s6 is used as an init system to handle signals so that docker stop and kill -s TERM properly shutdown the container. It is not used to run multiple processes.

Rationale: 
1. Alpine linux (very small but capable Linux distribution).
2. s6 for process management for both easily configurable, and highly stable images.

### Run

You can run the command below to create the container:

```bash
make
```


