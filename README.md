# .github
This is github actions template repo  

# available self-hosted runner labels 
sw-ubuntu-latest
sw-windows-latest

# gradle notes
You must add a step in your build.gradle to publish the artifacts.  
```
  // you must add this publishing block to your build.gradle 
       publishing {
         repositories {
             maven {
               name = "artifactory"
               url = "https://artifactory.sherwin.com/artifactory/sherwin-release-local"
               credentials {
                 username = System.getenv("ARTIFACTORY_USERNAME")
                 password = System.getenv("ARTIFACTORY_API_KEY")
               }
             }
```
