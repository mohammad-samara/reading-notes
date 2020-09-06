# Class-02

### Running JavaScript code outside of a browser?

 If you use Node.js to run JavaScript on your computer :

 - you can access files on your computer which you can't normally do with JavaScript, 
 - you can listen to network traffic on your computer, 
 - you can listen to HTTP requests that your machine gets and sends back a file, 
 - you can access databases directly.

### What is the difference between a module and a package?

 A **module** is a single JavaScript file that has some reasonable functionality ; A **package** is a directory with one or more modules inside of it.

### What does the node package manager do?
  * Online repository for the ***publishing of open-source Node.js projects***.
  * Command-line utility for ***interacting with said repository that aids in package installation, version management, and dependency management***. A plethora of Node.js libraries and applications are published on npm, and many more are added every day.

### Provide code snippets showing 3 different ways to export a function from a node module:

  * **Export Literals**:

1- `modules.exports = functionName()`

2- `modules.exports = {firstFunction() , secondFunction() }`

3- `export function functionName(){return 'some written code'}`

### Document the following Vocabulary Terms:

  * **Node.js**: is an open-source, cross-platform, JavaScript runtime environment that executes JavaScript code outside of a web browser.

  * **V8 Engine**: is Google's open source high-performance JavaScript and WebAssembly engine, written in C++. It is used in Chrome and in Node. js, among others. It implements ECMAScript and WebAssembly, and runs on Windows 7 or later, macOS 10.12+, and Linux systems that use x64, IA-32, ARM, or MIPS processors.

  * **module**: is a single JavaScript file that has some reasonable functionality.

  * **package**: is a directory with one or more modules inside of it.

  * **ecosystem**: is a managed lifecycle and dependency injection for the application components.

  * **node** package manager (npm): is an online repository for the publishing of open-source Node.js projects and a command-line utility for interacting with said repository that aids in package installation, version management, and dependency management.

  * **server**: is a computer program or a device that provides functionality for other programs or devices, called "clients".

  * **interpreter**: is the same as the complier but an interpreter directly executes the instructions in the source programming language while a compiler translates those instructions into efficient machine code.

  * **environment**: refers to the state of a computer, determined by a combination of software, basic hardware, and which programs are running. For example, if a program is running in a Windows environment, it means that the program is utilizing the Windows operating system.

  * **compiler**: is a program that translates code written in a high-level programming language (like JavaScript or Java) into low-level code (like Assembly) directly executable by the computer or another program such as a virtual machine.
