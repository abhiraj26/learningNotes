# Maven 

1. Download Maven from Maven Repo and add maven to the ClassPath.
2. Maven is convention over configuration unlike ant which is made better with the help of a build tool on top of it as Ivy. No need to define variables with unknown name. Have to define all the steps in order with cleam/compile/install and the main dir name etc. 
3. Structure of type :
    1. modelVerion : Currently 4.0.0
    2. groupId : Same as package names (Kept as com.company.etc)
    3. artifact Id : JavaConcepts (Project Name)
    4. version : 1.0-SNAPSHOT :- verion Number 
    5. packaging :- can be of type jar/tar 
4. Requires maven coomands are, mvn clean (Delete the target directory), mvn compile (To compile the jars for any compilation error)and mvn package (Create the .jar file with artifactId+version+packaging)

## Maven Structure 

1. Java Convention and requirement for maven.
    1. Java looks for src/main/java folder , it generates target after compiling and it looks for pom.xml file for configurations
    2. The package name exist in src/main/java , so for com.company com will come under src/main/java -> com -> company 
    3. Need to set up the src/test/java folder same as the source code pattern. (for Junit test)
    4. In target directory it genrates i. Classes (Compiled .class files) ii. surfire and test (For Unit Testing Output) iii. maven-artifacts which has package name iv. .jar file genrated after installing. 
2. pom.xml structure types :- 
    1. Project Info (groupId,artifactId,version,packaging)
    2. Dependencies
        1. Development Starts of SNAPSHOT, automaticall takes the latest changes (Not to a deploy to production with SNAPSHOT).
        2. Milestone Releases / Release Candidate (myapp-1.0-M1.jar | myapp-1.0-RC1.jar), Some people choose FINAL (myapp-1.0-FINAL.jar) for the final release.
        3. Packaging type can also be of pom which intakes other dependencies. 
        4. Transitive Dependencies (If we add hibernate-core it will add other dependencies it depends on like jpa, common-annotations etc.)
        5. Scopes by default is set to compile. (6 types of scope.<scope> test </scope> (test means will not be added in final artifact, only for tests.) )
    3. Build (Plugins, Dir Str)
        1. Can override final name by adding `<build> <final> NewName.tar </final> </build>`. We define all our plugins in this section.
    4. Repositories (Maven Central Repo / Internal Repos)
        1. Can add dependencies from different repos. Need to add yoour repos link in `<repository> </repository>`. The new changes come after saving the file.
    5. Plugins : 
        1. Goals : Can configure all clean,compile,test,package etc. It all is developed in super.pom , can be overriden. Goals are tied to phases. We write these code in `<execute><goals>` part in pom.xml, can make it to clean everytime we compile etc. 
        2. Phases : validate (Project has all neccesary details.), compile, integeration-test(Allow us to deploy and test code.) etc.
        Eg. Compiler Plugin Invokes javac, build the classpath set from dependencies. Defaults to java 1.5 regardless of our jdk version. In our pom `<configuration>` part we can set things like it can fork, change the memory settings and source and target dirs etc.
        
        3. Jar : Can include and exclude xml etc things in our jar file, manifest file
        4. Source : add Source to jar, source-jar in repo
        5. Javadoc : add JavaDoc to jar , can change the plugin to do it at some other phase like verify and install in the local repo.
3. Goals of Maven : 
    1. clean : delete target
    2. compile : add source code .class versions to classes and tests java files to tests
    3. package : add .jar file to target
    4. install : copy it to my local repo mvn install : /.m2/repo in form of (groupId)com/company/..   (It does what package does also.)
    5. tests : Run the tests in java
    6. deploy : Deploy it to repo.
  
