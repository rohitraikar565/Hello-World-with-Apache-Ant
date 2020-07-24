# Hello-World-with-Apache-Ant


md build\classes
javac -sourcepath src -d build\classes src\oata\HelloWorld.java
java -cp build\classes oata.HelloWorld

which will result in
Hello World

Creating a jar-file is not very difficult. But creating a startable jar-file needs more steps: create a manifest-file containing the start class, creating the target directory and archiving the files.

echo Main-Class: oata.HelloWorld>myManifest
md build\jar
jar cfm build\jar\HelloWorld.jar myManifest -C build\classes .
java -jar build\jar\HelloWorld.jar

Step  compile, package and run the application via

ant compile
ant jar
ant run
