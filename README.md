## Build Tools and Package Management

### Cheat Sheet
#### Maven
```
# Installation
# This will not install a conflicting openJDK version that comes as a dependencies of Maven
$ brew install --ignore-dependencies maven

# Build an artifact
# This will generate a "target" folder that contains the JAR file
$ mvn install

# Dependencies are managed in the "pom.xml" file
# The usual location of the downloaded dependencies from maven repository can be found at "~/.m2"

# Run the application
$ java -jar target/java-maven-app-1.1.0-SNAPSHOT.jar
```


#### Gradle
```
# Installation
$ brew install gradle

# Build an artifact
# This will generate a "build" folder, and inside it has "libs" folder that contains the JAR file
$ gradle build

# Dependencies are managed in the "build.gradle" file
# The usual location of the downloaded dependencies from maven repository can be found at "~/.m2"

# Run the application
$ java -jar build/libs/java-app-1.0-SNAPSHOT.jar
```

#### Node and NPM
```
# Installation
$ brew install node
$ node -v
$ npm -v

# Install dependencies
$ npm install
# You can use "npm" or "yarn" to install dependencies. These are package managers and NOT build tools
# Dependencies are managed in the "package.json" file
# There is a central repository called "npm repository" where we can download the dependencies

# Run the application
$ npm start

# Stop the application
$ npm stop

# Run tests
$ npm test

# Publish the artifact
# npm publish

# Package the app code and package.json in a tgz file
$ npm pack

# Build
# The command below will run "scripts.build" section in package.json, which is "webpack" in our case
# This will create the "server.bundle.js" file
$ npm run build
```

In Packaging Frontend Code
- You can create a separate package.json file for frontend and backend
- Or you can have a common package.json file
- Remember that Frontend/React Code needs to be transpiled
- Code needs to be compressed/minified
- There is a separate tool for building frontend artifacts e.g., webpack, grunt, and so on

Example Scenario: You have developed an application using ReactJS as the Frontend and Java as the Backend
- Bundle frontend app with webpack
- Manage dependencies with npm or yarn
- Package everything into a WAR file
