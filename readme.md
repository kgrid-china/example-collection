# Example KO Projects
This repository contains a collection of KGrid Knowledge Objects that demonstrate features 
of the grid, good development practices and useful tools.


- [Knowledge Object Project Anatomy](#anatomy-of-this-knowledge-object-project)
  * [Prerequisites](#rerequisites)
  * [Directories](#directories)
  * [Testing](#testing)
  * [Package](#package)
  * [Tools](#tools)
- [Example Projects](#example-projects)  

## Anatomy of this Knowledge Object project.
The following structure is not an requirement or enforced, it is a recommendation based 
on what the JavaScript and in particular Node community at large have been following by convention.

### Prerequisites
There are testing and packaging features in this project that require npm, npm is installed with Node.js
[npm](https://www.npmjs.com/get-npm).  Once npm is installed run  ```npm install``` at the root of this project.

### Directories

* **naan-name/** is intended for each knowledge object (e.g. _hello-world_)
* **tests/** is for all of your project test scripts
* **etc/** is a sub-directory for miscellaneous project
* **docs/** is a sub-directory for more detailed information about these KOs
* **dist/** is created and destroyed when running ```npm run package``` 
* **scripts/** is intended to capture various scripts need for the project (using [scripty](https://www.npmjs.com/package/scripty))
* **scriptswin/** windows versions of the scripts


### Testing 
Sample tests are located in the tests directory and can be executed using _npm_.  These tests utilize 
[Jest](https://jestjs.io/) and  [rewire](https://github.com/jhnns/rewire). est provides the testing 
framework and rewire allows the tests to access the javascript function without the 
convienace of the export modules (KGrid Javascript adaptor limitation).  The [tests](../tests) are in 
the tests directory.  You can execute the tests via npm

```
npm test
```

### Package 

You can create zip file of the Knowledge Object which can be used to deposit to a KGrid 
Library or load/activate on a KGrid Activator. 

```
npm run package
```

### Tools

*NPM Tool*
* [scripty](https://www.npmjs.com/package/scripty)
* [jest](https://jestjs.io/) 
* [rewire](https://github.com/jhnns/rewire)

## Example Projects 
* [Hello World Project](hello-world-project) - Simple project with one hello-world KO.  This is designed
 as a starting point. Demostrates a project structure the includes unit testing and scripts to package
 the KO deposit.

## List of other awesome KGrid Knowledge Object projects
Other interesting collections

* [Cancer Risk](https://github.com/kgrid-objects/cancer-risk)- Knowledge Objects of Cancer risk 
predictive models and risk score interpretations

* [Opioid Collection](https://github.com/kgrid-objects/mopen-opioid-collection) - This is a collection 
of KOs for KGrid that can be used to identify and report on certain features of opioid prescribing
