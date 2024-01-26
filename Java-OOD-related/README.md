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
  <a>
    <img src="resources/logo.png" alt="Logo" width="80" height="80">
  </a>
  <h3 align="center">Java OOD Related Q&A</h3>
</div>

<!-- TABLE OF CONTENTS -->
<details>
  <summary>Table of Contents</summary>
  <ol>
    <li><a href="#acess-level-private-protected-private-protected-public">Access Level: private, protected-private, protected, public</a></li>
    <li><a href="#final-key-word">final key word</a></li>
    <li><a href="#why-we-need-getter-and-setter">Why we need getter and setter</a></li>
    <li><a href="#equals-and-hashcode">equals and hashCode</a></li>
  </ol>
</details>

## Access Level: private, protected-private, protected, public

## final key word

## Why we need getter and setter

## equals and hashCode

People may encounter issues such as cannot see auto-grader output and get a 0 points. The issue is related to **Java Compile Time Error**, which is hidden from students' side. Typically, the error related to Java compile-time checking. Here I list a few of examples:

- Type Checking. Autograder may have a test case `mutiply(double val)`, however the submitted state it as `mutiply(int val)`;
- Wrong name of method. Autograder will directly call the function, so mis-typing function name may cause `symbols cannot found`;
- Forgot the `package` keyword when you declare a class inside a package;
- Wrong output type. Return a `double` but expected a `int` type, it will cause `Lossy conversion problem`;
- ...

Please double check your function signature, return type, output type, and also edge cases before submitting to GradeScope. Since it will not display the compile-time errors. If you cannot debug the issue, feel free to reach out to TAs to help you go through the code;
