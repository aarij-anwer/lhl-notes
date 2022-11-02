# Using process.argv

The simplest way of retrieving arguments in Node.js is via the `process.argv array`. This is a global object that you can use without importing any additional libraries to use it. You simply need to pass arguments to a Node.js application, just like we showed earlier, and these arguments can be accessed within the application via the process.argv array.

The first element of the process.argv array will always be a file system path pointing to the node executable. The second element is the name of the JavaScript file that is being executed. And the third element is the first argument that was actually passed by the user.