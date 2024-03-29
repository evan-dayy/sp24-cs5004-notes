<a name="readme-top"></a>

<!-- PROJECT LOGO -->
<br />
<div align="center">
  <a>
    <img src="resources/logo.png" alt="Logo" width="80" height="80">
  </a>
  <h3 align="center">IntelliJ IDEA Setting & Structure</h3>
</div>

<!-- TABLE OF CONTENTS -->
<details open>
  <summary>Table of Contents</summary>
  <ol>
    <li><a href="#set-up-file-structure-template">Set Up File Structure Template</a></li>
    <li><a href="#gradescope-autograder-not-working-issue">GradeScope Autograder Not Working Issue</a></li>
    <li><a href="#short-cut-to-make-life-easy">Short Cut to Make Life Easy</a></li>
    <li><a href="#jshell-java-in-terminal-for-quick-test">jshell: Java in Terminal for Quick Test</a></li>
    <li><a href="#why-we-need-pomxml">Why we need pom.xml</a></li>
  </ol>
</details>

## Set Up File Structure Template

Purpose of this section is to set up the project template so you don't need to move directory somewhere every time;

#### _let's first create a structure similiar to our assignment template, which is a project contains `src` and `test`, then you can create your own or preference :)_

- to make it simple, let's first create a folder anywhere you like, I prefer Desktop, I set the folder name as `assignment_template`;
- Open IntellJ IDEA, select `Open`

<div align="center">
  <img src="resources/r1.jpg" alt="image" >
</div>

- Select the folder you have just created, then click on trust project, you will enter the IntellJ UI;

<div align="center">
  <img src="resources/r2.jpg" alt="image">
</div>

- Right Click on `assignment_template` [a.k.a. the root folder], select `New` -> `Directory`, give name `src`, do the same thing for `test` folder, the following pic show the current status if you successfully reach to this step;

<div align="center">
  <img src="resources/r3.jpg" alt="image">
</div>

- Go to `Project Structure` located on `File` tab, set up your JDK, you can choose JDK-21, JDK-18 or any other to compile your files. In my case I will choose OpenJDK-20 since that is my regular setting.

<div align="center">
  <img src="resources/r4.jpg" alt="image">
</div>

<div align="center">
  <img src="resources/r5.jpg" alt="image">
</div>

- **This is an important step**. Go to Modules, first single click on `src`, you will notice that `Mark as: ....` row is lighted up, then select `Source`; This step mark you `src` as your source folder;

<div align="center">
  <img src="resources/r6.jpg" alt="image">
</div>

- Similarly, mark `test` as `Test` by singlely clicking on `test` then click `Test` on the `Mark as: ...` row, the result should be looks like the following pic; **Important Step!!!** Save the setting by click on `Apply` then `OK`;

<div align="center">
  <img src="resources/r7.jpg" alt="image">
</div>

- After the previus step, you will notice the `test` folder turns green!

<div align="center">
  <img src="resources/r8.jpg" alt="image">
</div>

- Go to the `File` -> `New Project Setup` -> `Save Project as Template...`;

<div align="center">
  <img src="resources/r9.jpg" alt="image">
</div>

- Give a name to your current template and add some description to remind you, then click `OK`;

<div align="center">
  <img src="resources/r10.jpg" alt="image">
</div>

- To use your template, close your IntellJ IDEA and reopn it, select `New Project`; In this case, I give a name `assignmentX`, which is a completed new project; you will notice on the left cornor, you can select your template!! then `Create`!

<div align="center">
  <img src="resources/r11.jpg" alt="image">
</div>

- We make it!!

<div align="center">
  <img src="resources/r12.jpg" alt="image">
</div>

- Let's Test it, add some code in it! It works!

<div align="center">
  <img src="resources/r13.jpg" alt="image">
</div>

- You can also save the project setting when you create the project using Maven Setting and then later on change it structure (ex. move the `test` directory outside and then save the template);)

## GradeScope Autograder Not Working Issue

People may encounter issues such as auto-grader failure without any output and get a 0 points. Most of time, the issue is related to **Java Compile Time Error**, which is hidden from students' side. Typically, the error related to Java compile-time checking. Here I list a few of examples:

- Type Checking. Autograder may have a test case `mutiply(double val)`, however the submitted state it as `mutiply(int val)`;
- Wrong name of method or missing of a method. Autograder will directly call the function, so mis-typing function name may cause `symbols cannot found`;
- Forgot the `package` keyword when you declare a class inside a package;
- Wrong output type. Return a `double` but expected a `int` type, it will cause `Lossy conversion problem`;
- Syntax errors ex. missing a semi-colon or a single bracket;
- Undeclared variable but you use it in the local;
- ...

Please double check your function signature, return type, output type, and also edge cases before submitting to GradeScope. Since it will not display the compile-time errors. If you cannot debug the issue, feel free to reach out to TAs to help you go through the code;

```
Meanwile, please exclude the hidden files when you submit it (such as .DS_Store);
Only upload and submit the files with .java extension;
```

**There are other factors may cause auto-grader failure**

- Wrong compression extension (.7z or other compression format instead of .zip);
- Wrong file structure. Make sure your submission follows the file strcture `src/package_name/...` and `test/testFile.java`;
- Structure format is listed here, **ONLY** select `src` and `test` at the same time and right click to zip them;

```text
 - src
    |
    |__ Package
            |___ B.java
            |___ A.java
 - test
    |__ testB.java
    |__ testA.java

```

- **DO NOT** put `src` amd `test` in an addtional folder and zip that folder, it will create an another level for auto-grader and lead to failure;



## Short Cut To Make Life Easy

#### _I will keep updating this session while exploring it_

- Generate `Getter`, `Setter`, `equals & hashcode`, `constructor` methods: `Command+N` for Mac & `Alt+Insert` for windows (sometimes you also need to `Alt+Fn+Insert`)

<div align="center">
  <img src="resources/r14.png" alt="image">
</div>

- Quick Search on class method and attributes `shift + shift` [tap shift double time]

<div align="center">
  <img src="resources/r15.png" alt="image">
</div>


## `jshell`: Java in Terminal for Quick Test

In python you can start a script and start defining variables or open a terminal and start typing like following:

```python
x = 10
print(x)
```

However, you cannot directly do this in Java since everything in Java is an Object (class), you should define everything in a class then to print it like following:

```java
class Printer {
  public static void main(String[] args) {
    int x = 10;
    System.out.println(x);
  }
}
```

It is complex and time-consuming if you just want to test some easy ideas, like what is `Integer.MAX_VALUE + 1`. Here, `jshell` is the best place to test your easy idea without declaring `class`, it is similar to type `python` or `python3` in terminal and test some easy code;

- Open terminal type the following:

```sh
$ jshell
```

- if it is installed, you would see following (most of jshell come with SDK so it should be installed):

```sh
$ jshell

|  Welcome to JShell -- Version 16.0.1

|  For an introduction type: /help intro


jshell>

```

- Here, you can define a variable just like `python` does without declaring a class! It is good way to test your simple idea quickly!

<div align="center">
  <img src="resources/r16.png" alt="image">
</div>

## Why we need `pom.xml`

`pom.xml` under Maven's project is a configuration file you set up a project. Remeber how you add `test cases` to the project? You are doing `Generate` -> `Test` -> `Generate Test Cases`; It is part of the IntelliJ's magic. However, a original way to do this is to mannually add `JUnit Dependency` to the `pom.xml`; It is good to know you can directly add dependecy to your project. Here I provide steps to add a JUnit Dependency mannually:

- Google `maven junit4 dependency`;

<div align="center">
  <img src="resources/r17.png" alt="image">
</div>

- Copy the code under Maven's Project, in this case it is the following code;

```xml
<!-- https://mvnrepository.com/artifact/junit/junit -->
<dependency>
    <groupId>junit</groupId>
    <artifactId>junit</artifactId>
    <version>4.12</version>
    <scope>test</scope>
</dependency>
```

- Go to `pom.xml`; Insert at the bottle:

```xml
<dependencies>
  <dependency>
      <groupId>junit</groupId>
      <artifactId>junit</artifactId>
      <version>4.12</version>
      <scope>test</scope>
  </dependency>
</dependencies>
```

- all the dependecies will be within the `<dependencies> .... </dependencies>` tag;
- Remember to reload all maven projects to apply these configurations!

<div align="center">
  <img src="resources/r18.png" alt="image">
</div>
