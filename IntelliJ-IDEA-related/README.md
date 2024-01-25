<!-- Improved compatibility of back to top link: See: https://github.com/othneildrew/Best-README-Template/pull/73 -->

<a name="readme-top"></a>

<!--
*** Thanks for checking out the Best-README-Template. If you have a suggestion
*** that would make this better, please fork the repo and create a pull request
*** or simply open an issue with the tag "enhancement".
*** Don't forget to give the project a star!
*** Thanks again! Now go create something AMAZING! :D
-->

<!-- PROJECT LOGO -->
<br />
<div align="center">
  <a href="https://github.com/othneildrew/Best-README-Template">
    <img src="resources/logo.png" alt="Logo" width="80" height="80">
  </a>
  <h3 align="center">IntellJ IDEA Setting & Structure</h3>
</div>

<!-- TABLE OF CONTENTS -->
<details>
  <summary>Table of Contents</summary>
  <ol>
    <li><a href="#set-up-file-structure-template">Set Up File Structure Template</a></li>
    <li><a href="#short-cut-to-make-life-easy">Short Cut to Make Life Easy</a></li>
  </ol>
</details>

## Set Up File Structure Template

Purpose of this section is to set up the project template so you don't need to move directory somewhere every time;

#### _let's first create a structure similiar to our assignment template, which is project contains `src` and `test`, then you can create your own or preference :)_

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
