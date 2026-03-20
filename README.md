Run

```bash
mvn validate
```

to reproduce the Maven Enforcer Plugin violation. You should see someting like

```
[ERROR] Failed to execute goal org.apache.maven.plugins:maven-enforcer-plugin:3.5.0:enforce (enforce-upper-bound-deps) on project spring-ws-1801-reproducer: 
[ERROR] Rule 0: org.apache.maven.enforcer.rules.dependency.RequireUpperBoundDeps failed with message:
[ERROR] Failed while enforcing RequireUpperBoundDeps. The error(s) are [
[ERROR] Require upper bound dependencies error for org.glassfish.jaxb:jaxb-runtime:4.0.6 [runtime] paths to dependency are:
[ERROR] +-com.example:spring-ws-1801-reproducer:0.0.1-SNAPSHOT
[ERROR]   +-org.springframework.ws:spring-ws-core:4.1.3
[ERROR]     +-org.glassfish.jaxb:jaxb-runtime:4.0.6 [runtime] (managed) <-- org.glassfish.jaxb:jaxb-runtime:4.0.7 [runtime]
[ERROR] , 
[ERROR] Require upper bound dependencies error for jakarta.xml.bind:jakarta.xml.bind-api:4.0.4 paths to dependency are:
[ERROR] +-com.example:spring-ws-1801-reproducer:0.0.1-SNAPSHOT
[ERROR]   +-org.springframework.ws:spring-ws-core:4.1.3
[ERROR]     +-jakarta.xml.bind:jakarta.xml.bind-api:4.0.4 (managed) <-- jakarta.xml.bind:jakarta.xml.bind-api:4.0.5
[ERROR] and
[ERROR] +-com.example:spring-ws-1801-reproducer:0.0.1-SNAPSHOT
[ERROR]   +-org.springframework.ws:spring-ws-core:4.1.3
[ERROR]     +-org.springframework:spring-oxm:6.2.17 (managed) <-- org.springframework:spring-oxm:6.2.17
[ERROR]       +-jakarta.xml.bind:jakarta.xml.bind-api:4.0.4 [runtime] (managed) <-- jakarta.xml.bind:jakarta.xml.bind-api:3.0.1 [runtime]
[ERROR] and
[ERROR] +-com.example:spring-ws-1801-reproducer:0.0.1-SNAPSHOT
[ERROR]   +-org.springframework.ws:spring-ws-core:4.1.3
[ERROR]     +-org.glassfish.jaxb:jaxb-runtime:4.0.6 [runtime] (managed) <-- org.glassfish.jaxb:jaxb-runtime:4.0.7 [runtime]
[ERROR]       +-org.glassfish.jaxb:jaxb-core:4.0.6 [runtime] (managed) <-- org.glassfish.jaxb:jaxb-core:4.0.6 [runtime]
[ERROR]         +-jakarta.xml.bind:jakarta.xml.bind-api:4.0.4 [runtime] (managed) <-- jakarta.xml.bind:jakarta.xml.bind-api:4.0.4 [runtime]
```
