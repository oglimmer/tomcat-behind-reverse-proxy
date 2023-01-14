FROM tomcat:10

# simple non-configurable configuration under /myapp
# access https://tomcat.local:8443/myapp/index.jsp
COPY src/main/webapps/ /usr/local/tomcat/webapps/myapp/

# simple non-configurable configuration under /
# access https://tomcat.local:8443/index.jsp
#COPY src/main/webapps/ /usr/local/tomcat/webapps/ROOT/

# path-configurable configuration under /fooapp
# access https://tomcat.local:8443/fooapp/index.jsp
#COPY src/main/webapps/ /opt/myapp/
#COPY context.xml /usr/local/tomcat/conf/Catalina/localhost/fooapp.xml

# path-configurable configuration under /
# access https://tomcat.local:8443/index.jsp
#COPY src/main/webapps/ /opt/myapp/
#COPY context.xml /usr/local/tomcat/conf/Catalina/localhost/ROOT.xml

# this is needed to add <Valve className="org.apache.catalina.valves.RemoteIpValve" httpServerPort="8000" httpsServerPort="8443" />
COPY server.xml /usr/local/tomcat/conf/
