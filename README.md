# ASP.NET Core Crash Course

## What is ASP.NET Core ?

* Microsoft C# tool to build web applications.
* Competitor to Java Spring, PHP Laravel, Python Flask, Node.js Express
* .NET - Microsoft's Software Development Platform since 2001. (similar to Java Virtual Machine).
* ASP stands for "Active Server Pages" - Dynamic web pages, usually connected to a database.
* Core - open source, cross-platform version of ASP.

## Where does C# fit into .NET ?

* .NET is NOT a language.
* The .NET framework consists of runtime engine and libraries for executing
programs written in a <u>compliant</u> language.
* The .NET framework is language neutral that supports more 20 langauges that include:
C#, C++, VB, Java/J++, Fortran, Ruby, Python, ...

## Why do we need ASP.NET ?

* Starting in 1997 (beginning of the Dot-com Bubble) there was a huge push away from fat client desktop applications and a migration toward browser based web applications.
* ASP.NET was Microsoft's answer in 2002 (end of Dot-com era) to Sun's maturing Enterprise Java Platform.
* ASP.NET replaced the Classic ASP (Active Server Pages) technology.

## A dynamic ASP.NET page

* An ASP.NET page is web page that contains a mix of HTML markup and dynamic ASP markup.
* An ASP.NET is run on the server, combining the static HTML code, and updating the dynamic ASP elements to produce a final HTML page
* An ASP.NET web page is also referred web forms

## Back End and Front End Options

* ASP.NET Core is Full Stack (Database, Business Logic, HTML)
* Can be combined with popular javascript front-end services:
    * React, Angular, Vue
    * Mobile apps

## Create project

* There we'll be applied MVC, which is full-stack ASP.NET type of project
* In order to create MVC project do the following:
	* Open Visual Studio and select <b>Create New Project</b>
	* On <i>Search for Templates</i> bar search <b>ASP.NET Core Web App (Model-View-Controller)</b>
	* For <i>Target Framework</i> select <b>.NET Core 3.1 (Long-term support)</b>
	* For <i>Authentication Type</i> select <b>Individual accounts</b> in order to generate interaction with Database
	* Check-in <i>Configure for HTTPS</i>
* In order to generate git ignore open command prompt within project directory and enter <b>dotnet new ignore</b> command

## MVC

* MVC stands for "Model, View and Controller"
* Model = classes (objects)
* View = web page (Razor HTML)
* Controller = connects models, business logic and web pages.

## Introduction to the MVC Design Pattern

The MVC desing pattern helps to enforce <u>separation of concerns</u> to help you avoid mixing presentation
logic, business logic, and data access logic together.

* Model: manages the behavior and data
* View: manages the display of data
* Controller: handles page events and navigation between pages

## View

* HTML CSS code (or similar)
* Usually gets a list of data from the controller.
* Dynamically combines data with HTML in a template
* Razor (ASP.NET)

## Model

* Data related
* Consists of classes/objects with properties.
* Uses SQL statements.
* Supplies the controller with lists of objects.

## Package Manager Console

* To access PM Console go to <b>Tools</b>-><b>NuGet Package Manager</b>-><b>Package Manager Console</b>
* Goal of the <b>Package Manager Console</b> is usually to install new dependencies, but also can be used for some database management

## Database Migrations

On PM Console enter <b>add-migration "initialsetup"</b>. It generated initialsetup file within migrations folder.

There are two options for creating databases with a system like this:
1. ORM - Object Relation Mapper:
	* Allow the computer to generate database tables based on classes defined in the application.
	* Database is updated using migrations.
	* <b>Entity</b> Framework is Microsoft's ORM.
	* Simple for basic applications.
2. DAO - Data Access Object:
	* Manually create tables.
	* Traditional method of database access.
	* Write your own SQL statements.
	* Database managers (DBA's) usually prefer DAOs.
	* Provides more visibility on finding problems.

ORM - Mapping here is between a class and a table.

Folder called Migrations is the language of creating tables

In order to update database migrations just run command <b>update-database</b> on PM Console
