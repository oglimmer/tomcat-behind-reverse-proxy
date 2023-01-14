# Tomcat behind a Reverse-Proxy

This is the project related to the medium article on https://oglimmer.medium.com/tomcat-behind-a-reverse-proxy-64666ec2f2be

# Limitations

As the docker documentation tells us ([here](https://docs.docker.com/network/host/)) `network=host` only works on Linux, thus this project has a linux or a macOS-windows folders.

Only on Linux you will see the actual source IP behind haproxy, anyhow you can still run this project on macOS or Windows, but you will always see the docker's network gateway IP as the source IP - just use your imagination in this case ;)

# How to run

```bash
docker-compose up --build
```

Modify your `/etc/hosts` by adding `127.0.0.1 tomcat.local`. 

You might also want to import haproxy/cert.pem to your Browser's trusted certificates.

## Linux:

Then access at http://localhost/myapp/index.jsp or http://tomcat.local/myapp/index.jsp

## macOS / Windows

Then access at http://localhost:8000/myapp/index.jsp or http://tomcat.local:8443/myapp/index.jsp

# Configurations

See tomcat/Dockerfile for different configurations.
