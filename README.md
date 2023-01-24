## Assimilate Java

### Day 2:  Setup Maven

* [Follow guide here for maven in five-minutes](https://maven.apache.org/guides/getting-started/maven-in-five-minutes.html)

`mvn --version`

The output should look like this:

```bash
@noahgift ➜ /workspaces/assimilate-java (main) $ mvn --version
Apache Maven 3.8.5 (3599d3414f046de2324203b78ddcf9b5e4388aa0)
Maven home: /usr/local/sdkman/candidates/maven/current
Java version: 17.0.5, vendor: Microsoft, runtime: /usr/lib/jvm/msopenjdk-current
Default locale: en_US, platform encoding: UTF-8
OS name: "linux", version: "5.4.0-1100-azure", arch: "amd64", family: "unix"
```

Create a project structure

`mvn archetype:generate -DgroupId=com.mycompany.app -DartifactId=my-app -DarchetypeArtifactId=maven-archetype-quickstart -DarchetypeVersion=1.4 -DinteractiveMode=false`

`cd my-app`

* Create a `Makefile`

* inside of the build, place a build command

```bash
build:
	mvn package
```

* Run `make build`

* Run hello world in Java by putting this into `Makefile` i.e. `make run`

```bash
java -cp target/my-app-1.0-SNAPSHOT.jar com.mycompany.app.App
```

Try out this hello world by doing the following:

```bash
make run
```

the output should look like this:

```bash
# run the app
java -cp target/my-app-1.0-SNAPSHOT.jar com.mycompany.app.App
Hello World!
```

To do a `make clean` and the rebuild we can combine all steps into a `make all`

```bash
make all
```


### Notes on setup for Java Devcontainer

* [created devcontainer](https://github.com/microsoft/vscode-remote-try-java/blob/main/.devcontainer/Dockerfile)
* Run `which java`

* Test out Java version: `java --version` and you should see something similar:

```
openjdk 17.0.5 2022-10-18 LTS
OpenJDK Runtime Environment Microsoft-6841604 (build 17.0.5+8-LTS)
OpenJDK 64-Bit Server VM Microsoft-6841604 (build 17.0.5+8-LTS, mixed mode, sharing)
```
* [Getting started with Java](https://dev.java/learn/getting-started-with-java/)

* build out hello world via `MyFirstClass.java` 