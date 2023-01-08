# Tomcat behind a Reverse-Proxy

This is the project related to the medium article on [https://oglimmer.medium.com/tomcat-behind-a-reverse-proxy-64666ec2f2be]()

# How to run

```bash
docker-compose up --build
```

Modify your `/etc/hosts` by adding `127.0.0.1 tomcat.local`. 

You might also want to import haproxy/cert.pem to your Browser's trusted certificates.

Then access at [http://localhost:8000/myapp/index.jsp]() or [http://tomcat.local:8443/myapp/index.jsp]()

# Configurations

See tomcat/Dockerfile for different configurations.
