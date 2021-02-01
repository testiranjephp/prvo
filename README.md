# Klika UpTime Tests

Klika UpTime Test is project for automate testing in Klika UpTime project. This project includes framework for testing wich is composed by UI and API part for testing. Goal of this readme file is to simplify process of using this framework for others developers and users who will use this framework for testing.

# Content
1.  [Contributors](#Contributors)
2.  [Prerequisites](#Prerequisites)
3.  [Getting started](#Getting-started)
    1.  [Download](#Download)
    2.  [Install](#Install)
    3.  [Clone project](#Clone-project)
    4.  [Crate personal access token on Azure DevOps](#Crate-personal-access-token-on-Azure-DevOps)
4.  [Runsettings file](#Runsettings-file)
5.  [How to run tests](#How-to-run-tests)
    1.  [Run tests from Visual Studio](#Run-tests-from-Visual-Studio)     
    2.  [Run tests from command line](#Run-tests-from-command-line)
6.  [Conclusion](#conclusion)


# Contributors 

Klika UpTime Test is part of Klika UpTime application that was made on Klika internship lasted from November 2020 to February 2021. This part of Klika UpTime project was made by two interns Kazazić Ilma and Zec Amir, under great support mentor Čengić Muris. Dautbegović Emrah also give himself contribution in the beginning of this project.

# Prerequisites

To start use this project and run tests you need few requirements. 

1.  Git - distributed version control system
2.  Visual Studio - free IDE with great support with wide spectre of tools that help us in ever-day job in developing and testing
3.  Personal acces token on Azure DevOps - it is a way how we can authenticate into Azure DevOps 

# Getting started

## Download

Git

1. Navigate your browser to  https://git-scm.com
2. Click on Downloads
3. Choose version for your OS

Visual Studio

1. Navigate your browser to https://visualstudio.microsoft.com/vs/
2. Click on Download Visual Studio dropdown list
3. Choose version you want to install 

> Note. It is recommended to install Visual Studio Community 2019 because it is published under free license for using.

## Install

Git 
Install Git for Windows

1. Open Git installer 
2. Go through installation wizard and use recommended settings
3. Check is Git installed with Git –version

Install Git for macOS
1. Open macOS Git installer 
2. Go through installation wizard and use recommended settings
3. Check is Git installed with Git –version

Install Git for Linux

Installing Git on Linux depends of distribution wich you want to use. For instruction how to install Git on Linux visit https://git-scm.com/download/linux and find your distribution.

## Clone project

Cloning project is actually downloading project on local machine. It is a way how you can run tests on your local computer. To clone Klika UpTime Tests project you need to follow these steps:

1. Navigate your browser to https://bitbucket.org/klika/workspace/projects/KUM
2. Click on uptime-tests repository
3. Click on Clone button
4. Copy link of repository
5. Open your terminal
6. Paste repository link in terminal and press enter

## Crate personal access token on Azure DevOps

Before you run your first test, you need to crate Personal Access Token on Azure Devops. To create this follow these steps:

1) Sign in to your organization in Azure DevOps (https://dev.azure.com/{yourorganization})
2) From your home page, open your user settings, and then select Personal access tokens.
3) And then select + New Token.
4) Name your token, select the organization where you want to use the token, and then choose a lifespan for your token.
5) Select the scopes for this token to authorize for your specific tasks.
6) When you're done, make sure to copy the token. For your security, it won't be shown again. Use this token as your password.
7) Copy this token in runsettings file ande save it.

# Runsettings file

Another important step before run tests is to include runsettings in Visual Studio. To do this follow next set of  instructions:

1) Click on Test from menu in Visual Studio  
2) Click on Configure Run Settings 
3) After this click on Select Solution Wide runsettings file
4) Locate runsettings file 
5) Click on Open

# How to run tests
To run tests from Visual Studio we use in Test Explorer. It is powerfull tool with a lot of different option for tests. 
To enable Test Explorer in Visual studio you have two option:

First way to enable it:
1. Click on **Test** in Visual Studio menu
2. When dropdown open choose **Test Explorer**

Second option is to use keyboard shortcut
1) Press **Ctrl + E** shortcut

## Run tests from Visual Studio
To run all test in solution, you have two option.

1) Click on **Run all tests** button in Test Explorer
2) Use shortcut **Ctrl + R**

To run specific tests you find test you locate test you want to run and you have two option to do this. 
1) Click on **Run button** in Test Explorer
2) Right click on test and select **Run** 


## Run tests from command line
You are not required to run tests only from Visual Studio IDE. You can use your command line for running tests. Visual Studio include VSTest.Console command line tool for running tests as an alternate way run test. 
To run tests from command you need to find VSTest.Console executable file in your terminal. Usually this file is located in Microsoft subfolder in Visual Studio in Program files

1) Open your terminal
2) Locate VSTest.Console and run in terminal

### How to run all tests

To run just one test we need to use /Tests option in VSTest.Console.

Example 
`vstest.console MyTests.dll /Tests:TestToRun`

### How to run all tests

To run multple tests from terminal we just specify test file in VSTest.Console
`vstest.console MyTests.dll` 

### How to specify runsettings file

When you need to specifiy runsettings file from terminal you can use /Settings option in VSTest.Console

Example

`vstest.console MyTests.dll /Settings:local.runsettings`  


# Conclusion
Idea of this readme file is to enable informations how to use this project. Because it is goal just basic informations, if you need detailed informations it is good to consult official documentation on  https://docs.microsoft.com/en-us/visualstudio/test/?view=vs-2019.

      

