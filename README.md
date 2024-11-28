# Experiment 05 : DevOps_Exploring-Containerization-and-Application-Deployment-with-Docker

<h1>Aim</h1>
<p>
  The objective of this experiment is to gain hands-on experience with the Maven build lifecycle by creating a simple Java project 
  and executing various Maven build phases.
</p>

<h1>Theory</h1>
<p>
  Maven is a widely-used build automation and project management tool in the Java ecosystem. 
  It provides a clear and standardized build lifecycle for Java projects, allowing developers to perform various tasks such as compiling code, 
  running tests, packaging applications, and deploying artifacts. This experiment aims to demonstrate the Maven build lifecycle and its different phases.
</p>

<h2>Key Maven Concepts</h2>
<ul>
  <li>
      <b>Project Object Model (POM):</b> The POM is an XML file named <code>pom.xml</code> that defines a project's configuration, dependencies, plugins, and goals. 
      It serves as the project's blueprint and is at the core of Maven's functionality.
  </li>
  <li>
      <b>Build Lifecycle:</b> Maven follows a predefined sequence of phases and goals organized into build lifecycles. 
      These lifecycles include clean, validate, compile, test, package, install, and deploy, among others.
  </li>
  <li>
      <b>Plugin:</b> Plugins are extensions that provide specific functionality to Maven. 
      They enable tasks like compiling code, running tests, packaging artifacts, and deploying applications.
  </li>
  <li>
      <b>Dependency Management:</b> Maven simplifies dependency management by allowing developers to declare project dependencies in the POM file. 
      Maven downloads these dependencies from repositories like Maven Central.
  </li>
  <li>
      <b>Repository:</b> A repository is a collection of artifacts (compiled libraries, JARs, etc.) that Maven uses to manage dependencies. 
      Maven Central is a popular public repository, and organizations often maintain private repositories.
  </li>
</ul>

<h2>Maven Build Lifecycle</h2>
<p>
  The Maven build process is organized into a set of build lifecycles, each comprising a sequence of phases. 
  Here are the key build lifecycles and their associated phases:
</p>
<h3>Clean Lifecycle</h3>
<ul>
  <li><b>clean:</b> Deletes the target directory, removing all build artifacts.</li>
</ul>
<h3>Default Lifecycle</h3>
<ul>
  <li><b>validate:</b> Validates the project's structure.</li>
  <li><b>compile:</b> Compiles the project's source code.</li>
  <li><b>test:</b> Runs tests using a suitable testing framework.</li>
  <li><b>package:</b> Packages the compiled code into a distributable format (e.g., JAR, WAR).</li>
  <li><b>verify:</b> Runs checks on the package to verify its correctness.</li>
  <li><b>install:</b> Installs the package to the local repository.</li>
  <li><b>deploy:</b> Copies the final package to a remote repository for sharing.</li>
</ul>
<h3>Site Lifecycle</h3>
<ul>
  <li><b>site:</b> Generates project documentation.</li>
</ul>
<p>
  Each phase within a lifecycle is executed in sequence, and the build progresses from one phase to the next. 
  Developers can customize build behavior by configuring plugins and goals in the POM file.
</p>

<h1>Materials</h1>
<ul>
  <li>A computer with Maven installed (<a href="https://maven.apache.org/download.cgi">https://maven.apache.org/download.cgi</a>)</li>
  <li>A code editor (e.g., Visual Studio Code, IntelliJ IDEA)</li>
  <li>Java Development Kit (JDK) installed (<a href="https://www.oracle.com/java/technologies/javase-downloads.html">https://www.oracle.com/java/technologies/javase-downloads.html</a>)</li>
</ul>

<h1>Experiment Steps</h1>
<h2>Step 1: Setup Maven and Java</h2>
<ul>
  <li>Ensure that you have Maven and JDK installed on your system. Verify their installations by running the following commands:</li>
</ul>
<pre>
  <code>
mvn -v
java -version
  </code>
</pre>

<h2>Step 2: Create a Maven Java Project</h2>
<ul>
  <li>Create a new directory for your project, e.g., <code>MavenDemo</code>.</li>
  <li>Inside the project directory, create a simple Java class, e.g., <code>HelloWorld.java</code>, with the following content:</li>
</ul>
<pre>
  <code>
public class HelloWorld {
public static void main(String[] args) {
  System.out.println("Hello, Maven!");
}
}
  </code>
</pre>
<ul>
  <li>Create a <code>pom.xml</code> file (Maven Project Object Model) in the project directory. Here's a minimal example:</li>
</ul>
<pre>
  <code>
<project xmlns="http://maven.apache.org/POM/4.0.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
xsi:schemaLocation="http://maven.apache.org/POM/4.0.0 http://maven.apache.org/xsd/maven-4.0.0.xsd">
<modelVersion>4.0.0</modelVersion>
<groupId>com.example</groupId>
<artifactId>MavenDemo</artifactId>
<version>1.0-SNAPSHOT</version>
</project>
  </code>
</pre>

<h2>Step 3: Explore the Maven Build Phases</h2>
<ul>
  <li>Clean Phase: To clean the project, run:</li>
</ul>
<pre>
  <code>mvn clean</code>
</pre>
<ul>
  <li>Compile Phase: To compile the Java source code, run:</li>
</ul>
<pre>
  <code>mvn compile</code>
</pre>
<ul>
  <li>Test Phase: To execute unit tests, run:</li>
</ul>
<pre>
  <code>mvn test</code>
</pre>
<ul>
  <li>Package Phase: To package the application into a JAR file, run:</li>
</ul>
<pre>
  <code>mvn package</code>
</pre>
<ul>
  <li>Install Phase: To install the project artifacts into your local Maven repository, run:</li>
</ul>
<pre>
  <code>mvn install</code>
</pre>
<ul>
  <li>Deploy Phase: To deploy artifacts to a remote Maven repository, configure your <code>pom.xml</code> and run:</li>
</ul>
<pre>
  <code>mvn deploy</code>
</pre>

<h2>Step 4: Run the Application</h2>
<ul>
  <li>After running the <code>mvn package</code> command, find the generated JAR file (e.g., <code>MavenDemo-1.0-SNAPSHOT.jar</code>) in the target directory. Run the application using:</li>
</ul>
<pre>
  <code>
java -cp target/MavenDemo-1.0-SNAPSHOT.jar HelloWorld
  </code>
</pre>

<h1>Conclusion</h1>
<p>
  This experiment demonstrates the Maven build lifecycle by creating a simple Java project and executing various Maven build phases. 
  Maven simplifies the build process by providing a standardized way to manage dependencies, compile code, run tests, and package applications. 
  Understanding these build phases is essential for Java developers using Maven in their projects.
</p>

