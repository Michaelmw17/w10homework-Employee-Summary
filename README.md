# Unit 10 OOP Homework: Template Engine - Employee Summary

### Licence

[![MIT license](https://img.shields.io/badge/License-MIT-blue.svg)](https://lbesson.mit-license.org/)


## Description

A Node CLI that takes in information about employees and generates a HTML webpage. This displays summaries for each employee. Designed with test driven development and OOP in mind. Easy way to keep track of team member details.

Oftentimes, *how* we design our code is just as important as the code itself. In this homework assignment, the challenge was to build a Node CLI that takes in information about employees and generates an HTML webpage that displays summaries for each person. Since testing is a key piece in making code maintainable, you will also be ensuring that all unit tests pass.

## Installation

1. Run

```
  npm i
```

2. Ensure command terminal is in correct directory
3. Run

```
node ./app.js
```

4. Follow the prompts


```As a manager
I want to generate a webpage that displays my team's basic info
so that I have quick access to emails and GitHub profiles
```

Ensure the following are correctly installed (if you have node already, make sure version is up to date):

- [Node.js](https://nodejs.org/en/)
- [inquirer](https://www.npmjs.com/package/inquirer)
- [jest](https://jestjs.io/)

Run npm install for the npm packages before running the CLI.

## Demonstration

* Below is an example of what your application may look like.

![Employee Summary 1](./assets/10-OOP-homework-demo-1.png)
![Employee Summary 2](./assets/10-OOP-homework-demo-2.gif)\
Or the full video is [here](./assets/10-OOP-homework-demo-3.mov)  

In the `Develop` folder, there is a `package.json`, so make sure to `npm install`.

The dependencies are, [jest](https://jestjs.io/) for running the provided tests, and [inquirer](https://www.npmjs.com/package/inquirer) for collecting input from the user.

There are also unit tests to help you build the classes necessary.

It is recommended that you follow this workflow:

1. Run tests
2. Create or update classes to pass a single test case
3. Repeat

🎗 Remember, you can run the tests at any time with `npm run test`

It is recommended that you start with a directory structure that looks like this:

```-
lib/           // classes and helper code
output/        // rendered output
templates/     // HTML template(s)
test/          // jest tests
  Employee.test.js
  Engineer.test.js
  Intern.test.js
  Manager.test.js
app.js         // Runs the application
```

### Hints

* Create multiple HTML templates for each type of user. For example, you could use the following templates:

  * `main.html`

  * `engineer.html`
  
  * `intern.html`
  
  * `manager.html`

* You will want to make your methods as pure as possible. This means try to make your methods simple so that they are easier to test.

* The different employee types should all inherit some methods and properties from a base class of `Employee`.

* In your HTML template files, you may want to add a placeholder character that helps your program identify where the dynamic markup begins and ends.

## Minimum Requirements

* Functional application.

* GitHub repository with a unique name and a README describing the project.

* User can use the CLI to generate an HTML page that displays information about their team.

* All tests must pass.

### Classes

The project  has  these classes: `Employee`, `Manager`, `Engineer`, `Intern`. The tests for these classes in the `tests` directory must all pass.

The first class is an `Employee` parent class with the following properties and
methods:

* Name
* id
* email
* getName()
* getId()
* getEmail()
* getRole() // Returns 'Employee'

The other three classes will extend `Employee`.

In addition to `Employee`'s properties and methods, `Manager` will also have:

* officeNumber

* getRole() // Overridden to return 'Manager'

In addition to `Employee`'s properties and methods, `Engineer` will also have:

* github  // GitHub username

* getGithub()

* getRole() // Overridden to return 'Engineer'

In addition to `Employee`'s properties and methods, `Intern` will also have:

* school

* getSchool()

* getRole() // Overridden to return 'Intern'

### User input

The project must prompt the user to build an engineering team. An engineering team consists of a manager, and any number of engineers and interns.

### Roster output

The project  generates a `team.html` page in the `output` directory, that displays a nicely formatted team roster. Each team member should display the following in no particular order:

* Name

* Role

* ID

* Role-specific property (School, link to GitHub profile, or office number)


## Questions / Contact

- Submit questions to my contact details below.
- App runs in CLI.


- Contact me with questions on my email: michaelmw17@outlook.com

## Resources

* [Constructor Docs](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Classes/constructor)

* [Prototype Docs](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object/prototype)

* [Class Docs](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Classes)

* [Jest Docs](https://jestjs.io/)

* [Bootstrap](https://getbootstrap.com/docs/4.0/getting-started/introduction/)
