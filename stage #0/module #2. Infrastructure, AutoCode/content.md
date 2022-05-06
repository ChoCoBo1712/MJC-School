# Infrastructure, AutoCode
## Must have to read
- [JVM vs. JRE vs. JDK: What is the Difference?](https://www.ibm.com/cloud/blog/jvm-vs-jre-vs-jdk "JVM vs. JRE vs. JDK: What's the Difference?")
- [Differences between JDK, JRE and JVM](https://www.geeksforgeeks.org/differences-jdk-jre-jvm/ "Differences between JDK, JRE and JVM")

## Setting up an environment. JDK/JRE/JVM

### JDK
An essential toolkit for Java development. The JDK includes:
an environment for executing Java programs called JRE. If you only need to run Java programs, without writing Java code, you can install the JRE separately.
a set of necessary utilities (javac, java debuggers, java docs, etc.). For example, the javac utility converts written code into intermediate byte code.

### JRE
Runtime environment for Java programs. Included in JDK by default. JRE contains core libraries, class loader, and JVM.

### JVM
A virtual machine that runs Java programs. It is part of the JRE. For each separate running Java program, its own JVM instance is created.

![](img/jdk-structure.png)

## Start Developing
To consolidate the material covered in this course, we will ask to write some task under the Autocode platform.
To confidently use these tools, we will need to learn following:
- How to compile and run Java application
- Git basics
- How to use Autocode for doing practical tasks
- **Advance:** What is Unit tests

### How to compile and run Java application
Currently, on large projects, they manually compile and assemble the project only in exceptional situations. To simplify the work, integrated development environments (IDE) are used to develop and run applications, as well as build tools and dependency management.

In this chapter, however, we will consider how to run Java code ourselves so that an understanding of how this process works is formed. But in the future, for convenience, we recommend using specialized tools, which we will analyze a little later.

#### To start building application we will need:
1. Install JDK.
2. Write first application.
3. Compile .java file to .class.
4. Run .class file

### Installing JDK
JDK is required for Java developers. It contains a Java compiler that allows you to compile your code written in Java in the byte code that JVM can understand. It also contains everything that you need to run Java applications.

#### To install JDK follow the next steps:
1. Go to https://www.oracle.com/java/technologies/downloads/. On the page, you can see there are several options. You can install the latest JDK version (currently it is JDK 18) or choose the earlier ones. I would recommend installing the latest one. You will have a new feature introduced in the latest version, and you will be able to run code from the previous versions like Java 8.
2. Choose a system you are working on. On the page, you will see Linux/macOS/Windows sections. Choose an appropriate one.
3. Find an option to download. You can download Java as an archive or as an installer.
4. Install or archive the downloaded file.
5. After installing, whether it is an archive or not, check the PATH environment variable. It should contain a path to the JDK bin directory. An example in window systems C:\java\jdk1.8.0_202\bin. The details may be found by the link
6. Set JAVA_HOME environment variable. Some third-party programs (for example IntelliJ Idea) expect this environment variable to be set to the installation directory of the JDK. JAVA_HOME should not include a bin directory in the path. An example in window systems C:\java\jdk1.8.0_202
7. Open Command Prompt and do the following commands (both the commands should run successfully and return the current version of the java installed in a system):
    - javac -version
    - java -version

### Writing first application
To write the first program, we need any text editor. While it won't be smart enough to tell errors or run our program, it's enough to write and work with Java.

In the old tradition, programmers start learning a new programming language by writing the "Hello World!" program. This program will simply print "Hello World!" to the console. We will simply provide code that you can copy, the meaning of which will be disassembled later.

    class HelloWorld {
      public static void main(String[] args) {
        System.out.println("Hello, World!"); 
      }
    }

Please copy these lines to a new file named HelloWorld.java. 
- As you can see, the file name is exactly the same as the class name inside the file `class HelloWorld`.
- To make it easier let's create a separate folder for that file, as an example we would take `C:\mjc-school`.

### Compiling .java file
1. Open CommandPrompt(CMD) as for Windows or similar for other Operating Systems.
   - Navigate to a new folder with HelloWorld.java file. We will use `cd C:\mjc-school`.
2. Compile Java file by doing command: `javac HelloWorld.java`.
   - In case you will have any issues, be sure that you correctly installed JDK in previous chapter, and you exactly copied lines above with same name of file.

As an outcome a new `HelloWorld.class` file will be generated.

### Running .class file
1. Open CommandPrompt(CMD) as for Windows or similar for other Operating Systems.
   - Navigate to a new folder with HelloWorld.java file. We will use `cd C:\mjc-school`.
2. Run Java file by doing command: `java HelloWorld`

### Installing IDE
As we have already discussed, as part of daily development, we do not always need to repeat these manual commands. For this we will use the IDE.

IntelliJ IDEA is the most popular IDE in the modern Java world, so in this section, we will consider installing this IDE. The IDE can be downloaded as Community or paid Ultimate version. All the most important features, that may need in development, exist in the Community version.

So, it is enough to install the Community version for now by the following steps:
1. Go to https://www.jetbrains.com/ru-ru/idea/download/
2. Choose your system Windows/macOS/Linux and a file type .exe or .zip and press the Download button for the Community version.
3. After it is downloaded, run the installer or archive in the appropriate folder.
4. After it finishes installing, you can run IntelliJ Idea and create your first project. Details may be found by the [link](https://www.jetbrains.com/ru-ru/idea/download/#section=windows)

At the end of this chapter we will provide advance topic related to usage of Intellij IDEA.

### Git. Version of control
The next topic we'll look at isn't just about Java development. The modern world of development is impossible without the use of a set of tools that directly affect the speed of writing and the quality of the product.

One such tool is the various Version Control Systems (VCS). We need to analyze the basic principles, since with the help of this technology we will solve practical problems. In the future, we will study VCS in detail, to the level necessary for a junior developer.

Version control system is a necessary tool for maintaining the history of changes in your files. After editing and saving the files, we want to see who made the changes and when, as well as be able to revert to any of the previous versions. For this, we need a version control system that allows us to navigate through the history of changes.

#### What is Git
Git is a free and open source distributed version control system designed to handle everything from small to very large projects with speed and efficiency.
**Source:** https://git-scm.com/

#### Gitlab and Github
**GitLab**: GitLab is a repository hosting manager tool that is developed by GitLab Inc and is used for the software development process. It provides a variety of management by which we can streamline our collaborative workflow for completing the software development lifecycle. It also allows us to import the repository from Google Code, Bitbucket, etc.

**GitHub**: GitHub is a repository hosting service tool that features collaboration and access control. It is a platform for programmers to fix bugs together and host open-source projects. GitHub is designed for the developers and to help them track their changes into a project through the repository. Following are some features of GitHub

You can see detailed difference using this [link](https://www.geeksforgeeks.org/difference-between-gitlab-and-github/ "link").

### Installing Git
The next important tool that should be installed is Git. Git is distributed version control system. Such web services like GitHub, GitLab, and others, where you can search committed code, are based on Git. Thus, installing Git is a required step if you want to push/pull any changes from a remote repository. It also might be useful when you are just working locally and would like to store the history of the changes.

To install Git on Windows, follow the next steps:
1. Go to https://git-scm.com/download/win and the download will start automatically.
2. Run the installer. Leave checkboxes and other settings as they are by default.
3. After the installing is done, run Command Prompt and perform the following command to make sure that Git was installed successfully:
    - git --version
      For other systems like Linux or macOS, the instructions may be found by the [link](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git "link").

You can find details tips at the end of the chapter.

### Installing Maven
// TODO: Add Maven
// TODO: Add screenshots

### How to use Autocode for doing practical tasks
While reading materials from that course you will be able to solve related practical tasks which will be prepared using Autocode platform.
Autocode has a well-formed documentation ([link](https://autocode-next.lab.epam.com/help/starting-work)), but we will discuss most needed steps.

1. Create your GitHub account.
2. Connect new account to Autocode.
3. Start doing task.
4. Using Intellij IDEA with git.
5. Submitting task.

#### Create your GitHub
In order to submit solutions you will need to have account on GitHub, it will be used to automatically fork task repository and then get final solution.
You can simply visit SignUp page: [GitHub](https://github.com/signup).

Follow instructions, most probably you will need to verify your email - please do it.

#### Connect account to Autocode
After you will have activated account you can start linkin you account to Autocode.
In order to link:
1. Log in to Autocode.
2. Click on you profile name, as e.g. `Ivan Ivanov`.
3. Click `profile`.
4. Click authorize for GitHub.
5. Confirm authorization in GitHub if needed.

#### Start doing task
When you will access course in autocode you will be able to see modules and tasks.
Select the task you want to start (Let's start doing `autocode-greetings` task) and use `Start` button. You will see some additional details here, such as minimum pass score, number of attempts and deadline.

The most import point is newly forked repository with small GitHub icon. 
This repository (you can click on it and see it on GitHub) will be used to check you solution. Every repository already contains small piece of code, you will need to extend it accordingly to task.

Let's start implementing your first task!

#### Using Intellij IDEA with git
Let's start from opening IDE and getting repository already created.
**In order to get repository:**
1. Open Intellij IDEA.
2. Select `Get from VCS`.
3. You will need to provide and URL from GitHub.
   - Open Autocode task.
   - Click on repository, you will be redirected to GitHub.
   - Click on button `Code`.
   - Copy URL.
4. Authorize to GitHub. As if most probably your first time accessing git from Intellij IDEA you will need to provide credentials or create a key. Follow the steps you will be prompted.

Finally, you should be able to see project structure:
- src
  - main
    - java
      - talks
        - mjc
          - FirstApplication.java
  - test
    - ...
- readme.md
- pom.xml

It is a typical structure for a Java project using Maven. Let's discuss key points here:
- `readme.md `- This file usually contains task description, where you can find some details of what should be done and how.
- `FirstApplication.java` - This file (or similar but with different naming) contains some basic logic to help you start implementing task. In this task you will need to make this file printing `Hello World!` into the console.

After carefully reading all the files and doing needed changes - you will need to publish you solution to GitHub.
This can be done using Intellij IDEA or via CommandPrompt.

#### Using Intellij IDEA
1. Press `CTRL + K`.
2. Select updated files, in our case it should be `FirstApplication.java`.
3. Add small commit message, usually it reflects changes done.
4. Press `Commit and Push`.
5. Confirm by clicking `Push`.

#### Using git
1. Open CommandPrompt(CMD) as for Windows or similar for other Operating System.
2. Navigate to project folder.
3. Use `git status` in order to see which files already included in commit.
4. In order to add file into commit you need to run `git add %FILE_NAME%`. And specify a file name, or you can simply do `git add .` - which means to add all files.
5. To commit use: `git commit -m "My first commit!"`. Where you need to replace "My first commit!" with commit message.
6. Then use `git push` in order to update GitHub repository with your local changes.

//TODO: Submitting task
//TODO: Advanced topics
### Unit testing. Junit
A unit test is a way of testing a unit - the smallest piece of code that can be logically isolated in a system. In most programming languages, that is a function, a subroutine, a method or property.

JUnit is a unit testing framework for Java programming language. It plays a crucial role test-driven development, and is a family of unit testing frameworks collectively known as xUnit. JUnit promotes the idea of "first testing then coding", which emphasizes on setting up the test data for a piece of code that can be tested first and then implemented. This approach is like "test a little, code a little, test a little, code a little." It increases the productivity of the programmer and the stability of program code, which in turn reduces the stress on the programmer and the time spent on debugging.

Sources:
--------
- https://smartbear.com/learn/automated-testing/what-is-unit-testing/
- https://www.tutorialspoint.com/junit/junit_overview.htm

Advance topic:
--------------
- [Using IntelliJ Idea for Java development](advanced/intelij-idea.md)
- [How to create first Git repository](advanced/create-repository.md)