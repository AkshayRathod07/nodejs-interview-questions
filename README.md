# nodejs-interview-questions

Q1. **What is Node.js?**
A1. Node.js is **neither a programming language nor a framework**. Instead, it is a **runtime environment for executing JavaScript code on the server side**. A runtime environment executes programs and is responsible for tasks like memory management and converting high-level languages (like JavaScript) to lower-level machine languages. Node.js was created by wrapping the **V8 JavaScript engine** (found in Chrome browsers) to allow JavaScript to run outside the browser, specifically on the server side.

Q2. **What is the difference between a framework and a runtime environment?**
A2. A **runtime environment** focuses on providing the necessary infrastructure for code execution, including basic services like memory management and input/output operations. Examples include cPython for Django (Python), JVM for Spring (Java), and CLR for .NET (C#). A **framework**, on the other hand, primarily focuses on simplifying the development process by offering a structured set of tools, libraries, best practices, reusable classes, and functions. Frameworks are like a wrapper over the runtime environment, adding additional features to make application development simpler for developers.

Q3. **What is the difference between Node.js and Express.js?**
A3. **Node.js is a runtime environment** that allows the execution of JavaScript code on the server side. **Express.js is a framework built on top of Node.js**, acting as a wrapper. Its purpose is to simplify the process of building web applications and APIs by providing features like a simple routing system and middleware support. Using Node.js with Express.js makes building server-side APIs very easy and fast.

Q4. **What are the differences between client-side and server-side?**
A4. The client-side, typically the **browser**, runs on the user's web browser, using languages like HTML, CSS, and JavaScript. It handles UI display, user interaction, and client-side logic. Objects like `document`, `window`, and `Navigator` are present.
The server-side, typically **Node.js**, runs on a server and primarily uses JavaScript. It handles business logic, data storage, access, authentication, and authorization. Objects like `request`, `response`, `server`, and `database` are present, but UI-specific objects (e.g., `document.getElementById`) are not.

Q5. **What are the seven main features of Node?**
A5. The seven main features of Node.js are:
1.  **Single-threaded**: Node.js applications are single-threaded.
2.  **Asynchronous execution**: Programs in Node.js execute asynchronously.
3.  **Event-driven**: Node.js applications are event-driven.
4.  **V8 JavaScript Engine**: Node.js uses the V8 JavaScript Engine from Google Chrome.
5.  **Cross-platform**: Node.js is cross-platform, allowing applications to run on any operating system.
6.  **NPM (Node Package Manager)**: Node.js has NPM to manage its dependencies.
7.  **Real-time capabilities**: Node.js is well-suited for bidirectional communication in real-time applications like chat and gaming.

Q6. **What is single-threaded programming?**
A6. Single-threaded programming refers to a process where a **single thread is responsible for starting tasks**. In a synchronous single-threaded model, this thread starts one task and waits for its completion before starting the next. Node.js can achieve asynchronous programming even with a single thread, where the single thread initiates tasks without waiting for their completion, allowing tasks to run concurrently.

Q7. **What is synchronous programming?**
A7. Synchronous programming means that **each task is performed one after the other**, sequentially. In this approach, one task must wait for the previous task to be completed, making it a **blocking approach**. This often leads to disadvantages in performance, as the total execution time is the sum of individual task times.

Q8. **What is multi-threaded programming?**
A8. In multi-threaded programming, when one thread starts a task and identifies another task, **a new thread is immediately created for the next task**. This allows multiple tasks to be executed **in parallel** by different threads. This approach is effective for CPU-intensive tasks that can utilize multiple processor cores, such as heavy desktop software. However, for internet APIs, multi-threaded approaches can lead to problems like deadlocks if not handled properly, which is why a single-threaded asynchronous approach is often preferred for JavaScript and Node.js applications.

Q9. **What is asynchronous programming?**
A9. Asynchronous programming in Node.js uses a **single thread to initiate tasks without waiting for their completion**. After initiating one task, the single thread immediately moves on to initiate the next task. This approach allows tasks to run concurrently, resulting in better time performance compared to synchronous operations, and it is a **non-blocking way** because tasks do not block the execution of subsequent tasks. Node.js achieves this through its single-threaded, non-blocking, and **event-driven architecture**. When a task is completed, it raises an event that the single thread listens to, allowing it to report completion and then resume other work.

Q10. **What is the difference between synchronous and asynchronous programming?**
A10.
*   **Synchronous Programming**: Tasks execute one after another. It is a **blocking approach**, meaning a task waits for the previous one to complete. This leads to **lower performance** and takes more time.
*   **Asynchronous Programming**: Tasks are initiated by a single thread without waiting for their completion, allowing them to run concurrently. It is a **non-blocking approach** where tasks do not block subsequent executions. This results in **improved performance** and faster execution times. Node.js fundamentally uses an asynchronous approach.

Q11. **What are events, event emitter, event Q, event Loop, and event driven in Node?**
A11.
*   **Event**: An event is a **signal or notification that something has happened** in a program, like an action being completed.
*   **Event Emitter**: The **source that generates or originates events**.
*   **Event Queue (Event Q)**: A queue where **all generated events are stored** in Node.js.
*   **Event Handler (Event Listener)**: A function that **performs code as per the event requirement** when an event is picked from the event queue. Developers write this code to handle events in their application.
*   **Event Loop**: The process of **picking up events one by one from the event queue in order** and processing them.
*   **Event-driven Architecture**: Node.js operations are **driven by or based on the events**, hence it is called event-driven.

Q12. **What are the main features and advantages of Node?**
A12. Node.js features and their corresponding advantages:
*   **Asynchronous Operation**: Enables handling multiple concurrent requests and non-blocking execution of threads.
*   **Google Chrome V8 JS Engine**: Executes code very quickly and fast.
*   **Event-driven Architecture**: Efficient in handling asynchronous operations and events, making it ideal for bidirectional communication in applications like chat and gaming.
*   **Cross-platform**: Supports deployment on various operating systems (Windows, Linux), enhancing application flexibility.
*   **JavaScript Language**: Allows developers to use the same language for both client-side and server-side development, eliminating the need to learn a new language.
*   **Scalability**: Due to the above features, Node.js is suitable for building scalable applications that can handle increased loads and easily grow with added features.

Q13. **What are the disadvantages of Node? When to use or when not to use Node?**
A13.
*   **When to use Node**: Node.js is ideal for **real-time applications** (e.g., chat applications, online gaming, collaborative tools) due to its event-driven architecture. It is excellent for building **lightweight and scalable REST APIs** that handle a large number of concurrent requests or connections. It's also a great choice for **microservices based architecture** due to its modular and scalable system.
*   **When not to use Node**: You should **not use Node.js in projects that demand CPU-intensive tasks**. Examples include video processing or software requiring heavy algorithms that would benefit from multi-threading, as multi-threaded technologies are better suited for utilizing multiple CPU cores and heavy servers. Node.js is single-threaded, making it less efficient for such tasks.

Q14. **How to set up a Node project?**
A14. (Note: The source explicitly states this is not an interview question, but a quick setup guide)
1.  Download and install Node.js from the internet.
2.  Download and install VS Code or any other code editor.
3.  Create a new folder (e.g., `myfirstproject`).
4.  Open VS Code and open the created folder.
5.  Open the terminal in VS Code and run the command `npm init -y`.
6.  Create a new JavaScript file (e.g., `app.js`) in your project folder.
7.  Run your Node.js application using the command `node app.js` in the terminal.

Q15. **What is npm? What is the role of Node modules folder in your project?**
A15. **NPM** stands for Node Package Manager, and its role is to **manage the `node_modules` folder** and the dependencies within your Node project. The **`node_modules` folder** contains all the libraries and dependencies that can be used in your Node project. These dependencies simplify development, and deleting them might cause project functionalities to stop working.

Q16. **What are Node modules?**
A16. Node modules refer to the **dependencies located in the `node_modules` folder** of a Node project. These are libraries that make development easier and simpler.

Q17. **What is the role of package.json file in Node?**
A17. The `package.json` file contains **project metadata**, which is information about your project. This includes details such as the project name, version, description, author, and license. It's typically found when you create your project for the first time.

Q18. **What are modules in Node? What is the difference between a function and a module?**
A18.
*   **Module in Node**: A module is a **piece of functionality** that can be easily reused within a Node.js application. Ideally, a single JavaScript file is treated as a single module.
*   **Difference between a function and a module**: A **module is a broader concept** that encapsulates functionality, serving as a feature implemented using functions. For example, in an e-commerce application, "orders" could be a module. A **function is a specific set of instructions or statements within that module**. A module can contain multiple functions and variables (e.g., an "order" module might have `getOrderList`, `submitOrder`, `postOrder` functions). While it's possible to put more than one module in a single JavaScript file, it's not a recommended approach.

Q19. **How many ways are there to export a module?**
A19. There are two main ways to export a module:
1.  **Using `module.exports` object**: `module.exports.functionName = functionName` (or for variables/objects).
2.  **Direct export using `exports` object**: `exports.functionName = functionName` (or `exports.variableName = variableName`, etc.). This is a shortcut approach where separate export statements are not needed.

Q20. **What will happen if you do not export the module?**
A20. If you do not export the module, then the module's functions, variables, or objects **will not be available or accessible outside that module's JavaScript file**.

Q21. **How to import single or multiple functions from a module?**
A21. To import functions, you use the **`require` function**, which is an inbuilt Node.js function.
*   **Importing a single function (when only one function is exported using `module.exports = functionName`)**: You can use `const myFunc = require('./myModule')` and then call `myFunc(parameter)`. Node automatically detects the single exported function.
*   **Importing multiple functions (or specific named exports)**: You should use `const { functionName1, functionName2 } = require('./myModule')` and then call `functionName1(parameter)`. This requires providing the function name because there are multiple functions.

Q22. **What is module wrapper function?**
A22. In Node.js, each module is **automatically wrapped in a function** by Node.js before it is executed. This is called the module wrapper function. Developers do not need to write this function themselves; its purpose is to simplify and shorten code for developers. This explains why code in an `app.js` file can execute without being explicitly put inside a function.

Q23. **What are the types of modules in Node?**
A23. There are three types of modules in Node.js:
1.  **Built-in Modules (Core Modules)**: These are modules already present in Node.js that provide essential, common functionalities (e.g., `fs` for file system, `http` for HTTP server, `path`, `os`, `events`). You just import and use them.
2.  **Local Modules (User-defined Modules)**: These are modules developed by developers as per their project requirements. Developers create, export, and use their functions in other files within their project.
3.  **Third-party Modules**: These are external packages or libraries created by the community to provide additional functionalities. They need to be installed first using `npm install` commands (e.g., `npm install lodash`) before they can be used in your application.

Q24. **What are the top five built-in modules commonly used in Node projects?**
A24. The top five commonly used built-in modules in Node projects are:
1.  **FS Module** (File System)
2.  **Path Module**
3.  **OS Module** (Operating System)
4.  **Events Module**
5.  **HTTP Module**

Q25. **Explain the role of the FS module. Name some functions of it.**
A25. The **FS (File System) module** in Node.js provides a set of methods for **interacting with the file system**, primarily for managing files.
Some functions of the FS module include:
*   `readFile`: Used to read the contents of a file asynchronously.
*   `writeFile`: Used to write content to a file.
*   `appendFile`: Used to append new data to existing file data.
*   `unlink`: Used to delete a specified file.
*   `readdir`: Used to read the content of a directory.
*   `mkdir`: Used to create a new directory (folder).
*   `rmdir`: Used to remove a specified folder (directory).

Q26. **Explain the role of the Path module. Name some functions of it.**
A26. The **Path module** provides utilities for **joining, resolving, parsing, formatting, normalizing, and manipulating file and directory paths** (or URLs). It helps in handling path strings consistently across different operating systems.
Some functions of the Path module include:
*   `join`: Used to join folder and file names to create a full path.
*   `parse`: Used for parsing a path string into an object containing properties like root, dir, base, ext, and name, making it easier to understand and reuse parts of the path.
*   `basename`: Returns the last portion of a path.
*   `dirname`: Returns the directory name of a path.
*   `extname`: Returns the extension of the path.
*   `resolve`: Resolves a sequence of path segments into an absolute path.
*   `normalize`: Normalizes the given path, resolving '..' and '.' segments.

Q27. **Explain the role of the OS module. Name some functions of it.**
A27. The **OS module** in Node.js projects provides a set of methods for **interacting with the underlying operating system** on which the Node application is running. This information is useful for making applications cross-platform, allowing them to perform functionalities specific to different operating systems.
Some functions of the OS module include:
*   `type`: Provides the type of the operating system (e.g., 'Windows_NT', 'Linux').
*   `userInfo`: Gets user information of the operating system.
*   `totalmem`: Provides the total memory of the operating system in bytes.
*   `freemem`: Provides the free memory available in the operating system in bytes.

Q28. **Explain the role of Events module. How to handle events in Node?**
A28. The **Events module** is crucial for Node.js's **event-driven architecture**, enabling the creation and handling of custom events. It provides the `EventEmitter` class, which is used to emit and listen for events.
To handle events:
1.  **Import the `events` module** and get the `EventEmitter` class.
2.  **Create an instance** of `EventEmitter` (e.g., `myEmitter = new EventEmitter();`).
3.  **Register an event listener** using the `on` function (e.g., `myEmitter.on('eventName', callbackFunction)`). The callback function defines the logic to execute when the event occurs.
4.  **Emit the event** using the `emit` function (e.g., `myEmitter.emit('eventName')`). When this happens, the registered listener for `eventName` will be triggered.
It's important to register the event listener *before* emitting the event.

Q29. **What are event arguments?**
A29. **Event arguments** are **additional information or parameters that can be passed along with an event** when it is emitted. These arguments are received by the parameters of the callback function registered as the event listener. They allow for passing data along with the event, which can then be used inside the event handling logic as per application requirements.

Q30. **What is the difference between a function and an event?**
A30. A **function is a reusable piece of code** that performs a specific task when it is called. An **event, on the other hand, represents an action** that has happened (e.g., a request coming to an API). Internally, events can trigger the execution of single or multiple functions to perform tasks. So, events signify *what* happened, and functions define *how* to respond to it.

Q31. **What is the role of HTTP module in Node?**
A31. The **HTTP module** in Node.js is one of the most important modules, primarily used to **create an HTTP server**. This server listens to incoming HTTP requests from clients (like UI servers) at a specific URL and port number on the internet, processes them, and then sends back HTTP responses to the clients. It acts as the backbone for receiving and sending web communications.

Q32. **What is the role of `createServer` method of the HTTP module?**
A32. The `createServer` method of the HTTP module in Node.js is specifically used to **create an HTTP server**. This method accepts a callback function as a parameter, which defines the logic to be executed when a request is received and before a response is sent. After creating the server, the `listen` method is used on the server object to enable it to listen for incoming requests on a specified port number.

Q33. **What are the advantages of using Express with Node?**
A33. Four advantages of using Express with Node are:
1.  **Simplifies Web Development**: Like other frameworks, Express provides many built-in methods and features that streamline the software development process.
2.  **Middleware Support**: Express makes managing multiple middlewares easy, which are crucial for handling requests and responses properly, especially for millions of requests.
3.  **Flexible Routing System**: It provides a simple way to understand URL patterns and redirect incoming requests to appropriate REST API methods (e.g., `GET`, `POST`) with minimal code.
4.  **Template Engine Integration**: Express simplifies the process of creating dynamic HTML content on the server side by allowing easy integration with template engines, combining HTML templates with data.

Q34. **How do you install Express in a Node project?**
A34. (Note: The source explicitly states this is not an interview question)
To install Express, open the terminal in your code editor (e.g., VS Code) and run the command: `npm install express`. This will install the Express framework, allowing you to use its features in your project.

Q35. **How to create an HTTP server using Express.js?**
A35. Creating an HTTP server with Express.js is a four-step process:
1.  **Import Express**: `const express = require('express');`.
2.  **Create an Express application instance**: `const app = express();` (This creates your server).
3.  **Set the port number**: Choose a port, e.g., `const port = 3000;`.
4.  **Start the Express server**: Call the `listen` method on the app server: `app.listen(port, () => { console.log('Server running...'); });`.

Q36. **How do you create and start the Express application?**
A36.
*   To **create an Express application**: First, import the Express module, then call the `express()` function to create the server instance, typically assigned to an `app` variable (e.g., `const app = require('express')();`).
*   To **start the server or listen to requests**: Call the `listen` method of the application server. This method takes the port number as the first parameter and an optional callback function (e.g., a message to log) as the second parameter.

Q37. **What is middleware in Express.js and when to use them?**
A37. **Middleware in Express.js is a function** that handles HTTP requests, performs operations on them, and then passes control to the next middleware function in a sequence. It acts as a "middleman" between the incoming request from the front end and the application's final endpoints (like `GET`, `POST`, `PUT`, `DELETE` methods).
**When to use them**: Middlewares are used for common functionalities that apply to almost all requests in an application. Examples include:
*   Logging request details.
*   Authenticating or validating requests.
*   Implementing security measures.
*   Managing multiple requests efficiently.
Together, these middlewares form a **request pipeline**.

Q38. **How to implement middleware in Express?**
A38. Implementing middleware in Express involves four steps:
1.  **Initialize an Express application**: `const app = express();`.
2.  **Define a middleware function**: This function accepts three parameters: `request`, `response`, and `next` (a callback function). The `next` function is crucial for passing control to the next middleware in the stack.
3.  **Execute or "call" the middleware**: Use the `app.use()` method, passing the middleware function's name as an argument (e.g., `app.use(myMiddleware);`). This makes the middleware execute when a request is received.
4.  **Start the server**: Use `app.listen()` to enable the server to listen for incoming requests.

Q39. **What is the purpose of the `app.use` function in Express?**
A39. The `app.use` method of the Express application server is used to **execute middleware globally** and **for all incoming requests** (e.g., `GET`, `PUT`, `POST`, `DELETE` methods). This means the specified middleware will be applied to every request, regardless of its method or specific URL path.

Q40. **What is the purpose of the `next` parameter in Express.js?**
A40. The `next` parameter in an Express middleware function is a **callback function**. Its purpose is to **pass control to the next middleware function in the stack** or to the final route handler. If `next()` is not called at the end of a middleware function, the request-response cycle will be halted, and subsequent middlewares or route handlers will not be executed. This function is an inbuilt feature of the Express framework.

Q41. **How to use middleware globally for a specific route?**
A41. To execute middleware only for a **specific URL path** (or "route") globally (meaning for all HTTP methods like `GET`, `POST`, etc.), you use the `app.use()` method. However, this time, you pass the specific URL path as the *first* argument, followed by the middleware function as the *second* argument (e.g., `app.use('/example', myMiddleware);`). This ensures the middleware only runs if the request URL contains the specified string.

Q42. **What is the request pipeline in Express?**
A42. The **request pipeline in Express is a series of middleware functions** that handle incoming HTTP requests. Requests pass through each middleware function sequentially, with each middleware potentially performing some operation on the request or response, before finally reaching the application's end points (e.g., `GET`, `POST` methods). It's called a "pipeline" because requests flow through it like through a pipe.

Q43. **What are the types of middlewares in Express.js?**
A43. There are five main types of middlewares in Express.js:
1.  **Application-Level Middleware**
2.  **Router-Level Middleware**
3.  **Error Handling Middleware**
4.  **Built-in Middlewares**
5.  **Third-party Middlewares**

Q44. **What is the difference between Application Level and Router level middleware?**
A44.
*   **Application-Level Middleware**: This middleware is executed **globally for all incoming requests and for all URLs** in your application. It's common for all requests to the application. It's typically applied using `app.use(middlewareFunction)`.
*   **Router-Level Middleware**: This middleware is executed **only for a specific URL** (or "route"). It's applied using `app.use('/specific-url', middlewareFunction)`.

Q45. **What is error handling middleware and how to implement it?**
A45. **Error handling middleware** is designed to **capture and properly log error details**, and then send a suitable, user-friendly message to the user or client in case an error occurs during application execution.
**Implementation**: An error handling middleware is defined as a function that accepts **four parameters**: `err` (the error object), `request`, `response`, and `next`. The presence of the `err` parameter differentiates it from regular middleware. When an error occurs in a preceding middleware or route handler, Express.js automatically passes the error to the next error-handling middleware in the stack. Inside this middleware, you typically log the error details (e.g., stack trace) and send an appropriate error message and status code back to the client.

Q46. **If you have five middlewares then in which middleware you will do the error handling?**
A46. You should **always handle the error object in the last middleware**. This is because if an error occurs in any preceding middleware (e.g., the second middleware), Express.js will **directly jump and execute the next middleware that has an error handling code**, skipping any regular middlewares in between. Therefore, to ensure no error is missed, it should be in the final middleware.

Q47. **What is built-in middleware? How to serve static files from the Express.js?**
A47. **Built-in middleware** refers to **in-built functions provided by the Express framework** itself to simplify developers' work; they do not need to be installed or coded by the developer.
To **serve static files** (like images) from an Express.js application, you use the `express.static()` built-in middleware. You call this static function inside the `app.use()` method, passing the folder name where your static files are located (e.g., `app.use(express.static('public'));`). This makes all files inside the specified folder (e.g., `public`) directly accessible via URL without authentication.

Q48. **What are third-party middleware? Give some examples.**
A48. **Third-party middlewares** are **external packages or libraries created by the community**, not part of the Express framework itself, nor created by the application developer. To use them, you must first **install them using `npm install`** (e.g., `npm install helmet body-parser compression`). After installation, you import and then call them inside the `app.use()` method.
Examples and their purposes:
*   **Helmet**: Used for setting HTTP security headers.
*   **Body-parser**: Used to parse incoming request bodies.
*   **Compression**: Used for compressing HTTP responses to improve performance.

Q49. **Can you summarise all the types of middlewares?**
A49.
*   **Application-Level Middleware**: Executes globally for all requests in the application.
*   **Router-Level Middleware**: Executes only for specific URLs or routes.
*   **Error Handling Middleware**: Handles errors using a special four-parameter signature (`err, req, res, next`).
*   **Built-in Middleware**: In-built functions provided by Express (e.g., `express.static`, `express.json`, `express.urlencoded`).
*   **Third-party Middleware**: External packages installed via npm (e.g., `helmet`, `body-parser`, `compression`).

Q50. **What are the advantages of using middlewares in Express.js?**
A50. The advantages of using middlewares in Express.js include:
*   **Modularity**: Middlewares are like small, reusable functions or modules that perform specific tasks, promoting modular design.
*   **Reusability**: The same middleware can be reused in multiple places within an application, making the code easier to maintain.
*   **Improved Request Handling**: Middlewares allow for better handling of requests and responses, such as validating incoming request content.
*   **Flexible Control Flow**: Developers can decide which middleware applies to which route or request type, offering flexible control.
*   **Third-Party Middlewares**: Access to a wide range of community-developed middlewares simplifies the implementation of various features and enhances application functionality.

Q51. **What is routing in Express?**
A51. **Routing in Express is the process of directing incoming HTTP requests to the appropriate handler functions**. This direction is based on the **request method** (e.g., `GET`, `POST`) and the **URL path**. It determines which specific controller method should execute for a given request (e.g., `/orders` URL with a `GET` method goes to `getOrders` method).

Q52. **What is the difference between middleware and routing in Express?**
A52.
*   **Middleware**: A **function** that intercepts HTTP requests. It can access request and response objects, perform actions like authorization or logging, and either end the request-response cycle or pass control to the next middleware or route handler. Middleware performs logic on requests.
*   **Routing**: A **process** of directing incoming HTTP requests to the correct "handler functions" (like `GET`, `POST`, `PUT`, `DELETE` methods) based on the request method and URL path. Routing *directs* the request but does not perform any business logic on the request itself.

Q53. **How to implement routing? How do you define routes in Express?**
A53. Routing is implemented by **defining routes** in your application.
To define routes:
1.  Create an instance of the Express application (e.g., `const app = express();`).
2.  Use `app.methodName()` (e.g., `app.get()`, `app.post()`, `app.put()`, `app.delete()`) to define a route.
3.  This method accepts two parameters:
    *   The **route path** (e.g., `'/'` for the root path, `'/login'` for a specific URL).
    *   A **callback function** (also called a "route handler"). This function contains the logic to be executed when a request matches the defined route.
For example: `app.get('/', (req, res) => { res.send('Hello World'); });`.

Q54. **How to handle routing in Express real applications?**
A54. In real applications, routing often involves these steps:
1.  **Import the Express application instance**.
2.  **Define and execute middlewares** (e.g., for authentication, logging).
3.  **Import controllers**: These files contain the business logic (e.g., `getOrders`, `postOrders`).
4.  **Define routes to redirect requests to controllers**: Use `app.methodName('/url', controller.functionName)` to map URLs and methods to specific controller functions (e.g., `app.get('/orders/:id', orderController.getOrderById);`).
5.  **Start the server**. This approach promotes separation of concerns and organizes code better.

Q55. **What are route handlers?**
A55. **Route handlers** are the **callback functions** that are passed as the **second argument when defining a route** using methods like `app.get()`, `app.post()`, etc.. Their purpose is to **process the incoming request and generate the appropriate response**. All the logic for handling a specific route (e.g., fetching data from a database, performing calculations) is written inside these functions.

Q56. **What are route parameters in Express?**
A56. **Route parameters** are **dynamic values within a URL path** that are sent by the user with the request. They are defined in the route path using a colon (e.g., `/users/:userId`). You can access these dynamic values using the `request.params` object (e.g., `req.params.userId`) within your route handler function, and then use them as needed by your application.

Q57. **What are router object and router methods and how to implement**Create a router object**: `const router = express.Router();`.
2.  **Define routes on the router object**: `router.get('/path', handlerFunction);`.
3.  **Export the router**: `module.exports = router;`.
4.  **Import and mount the router in your main application file (`app.js`)**: Use `app.use('/api', myRouter);`. Mounting means the routes defined in `myRouter` will only run under the `/api` URL prefix. This approach promotes modularity and reusability of routes across different files.

Q58. **What are the types of router methods?**
A58. The types of router methods are:
*   `router.get()`: For handling `GET` requests.
*   `router.post()`: For handling `POST` requests.
*   `router.put()`: For handling `PUT` requests.
*   `router.delete()`: For handling `DELETE` requests.

Q59. **What is the difference between `app.get` and `router.get` methods?**
A59.
*   **`app.get()`**: Used to define routes **directly on the main Express application object** (`app`). Routes defined this way are automatically mounted on the root path. This approach can lead to unstructured and unorganized code in large applications, and these routes are **not easily reusable** in other parts of the application.
*   **`router.get()`**: Used to define routes on a **separate router object** (created with `express.Router()`). These routes are *not* automatically mounted; they must be explicitly exported and then mounted onto the main application object using `app.use()`. This method is preferred in large applications as it promotes **modularity, code organization, and reusability** of routes across different files or modules.

Q60. **What is `express.Router` in Express.js?**
A60. `express.Router` is a **class in Express.js that returns a new router object**. This router object acts as a mini-Express application, specifically designed for handling routes. It allows developers to define routes in separate, modular files, which can then be exported and mounted into the main application, improving code organization and reusability.

Q61. **Share a real application use of routing.**
A61. A real application use of routing involves combining it with middleware, such as for **authenticating requests based on a token**.
For example:
1.  Create a router object: `const router = express.Router();`.
2.  Define an authentication middleware function.
3.  Use a router method to apply this middleware to a specific "protected" route: `router.get('/protected', authenticationMiddleware, (req, res) => { /* protected logic */ });`.
4.  Mount this router under a base path in the main application: `app.use('/api', router);`.
Now, any request to `/api/protected` will first pass through the `authenticationMiddleware`. If no valid authentication token is present, the middleware can return an "unauthorized" error.

Q62. **What is route chaining in Express?**
A62. **Route chaining** means you can **define multiple route handlers (middlewares) for a single route**. This allows for executing a sequence of middleware functions one by one for a specific route. For example, `app.get('/single-root', middleware1, middleware2, finalHandler);`. This concept promotes modularity, organizes code, improves readability, and separates concerns by allowing various processing steps for a route to be defined in a clear sequence.

Q63. **What is route nesting in Express?**
A63. **Route nesting** is an organizational approach in Express.js that **groups related routes hierarchically under a common URL prefix**. For instance, all routes related to users (like `/users/profile`, `/users/settings`) can be "nested" inside a `/users` root. This allows for creating more modular and structured code, making the codebase easier to manage and maintain, especially in applications with many routes.

Q64. **How to implement route nesting in Express?**
A64. To implement route nesting:
1.  **Define related routes in separate files using `express.Router()`**: For example, create `userRouter.js` for all `/users` related routes (e.g., `router.get('/profile', ...)`) and `productsRouter.js` for `/products` related routes.
2.  **Export these individual routers** from their respective files.
3.  **Import and mount these routers in your main application file (`app.js`)**: Use `app.use()` to associate the routers with their common URL prefixes (e.g., `app.use('/users', userRouter);` and `app.use('/products', productsRouter);`). This way, `userRouter` handles all requests starting with `/users`, and `productsRouter` handles those starting with `/products`.

Q65. **What are template engines in Express?**
A65. **Template engines are libraries that enable developers to generate dynamic HTML content** by combining static HTML templates with data. While Node.js REST APIs primarily handle business logic and data, template engines are used in scenarios (like server-side rendering) where the Node.js application needs to send a complete HTML document. They merge data (e.g., from a database) into placeholders within an HTML template to produce the final dynamic HTML.

Q66. **Name some template engine libraries.**
A66. Some popular template engine libraries include:
*   **EJS** (Embedded JavaScript) - most popular
*   **Handlebars**
*   **Pug**
*   **Mustache**
*   **Nunjucks** (Njkx)

Q67. **How to implement EJS templating engine in Express application?**
A67. Implementing EJS templating engine involves five steps:
1.  **Install EJS**: `npm install ejs` (since it's a third-party module).
2.  **Create a `views` folder** and an HTML template file (e.g., `index.ejs`) inside it. The template will contain static HTML and placeholders for dynamic data (e.g., `<%= title %>`).
3.  **Set the view engine in your Express application**: In your `server.js` (or `app.js`) file, use `app.set('view engine', 'ejs');`.
4.  **Set the views directory**: Specify where the view engine should look for templates: `app.set('views', path.join(__dirname, 'views'));` (using the `path` module).
5.  **Render the template with data**: In a route handler, use the `response.render()` method to combine the template with dynamic data: `res.render('index', { title: 'My Application Data' });`.

Q68. **What are REST and RESTful API?**
A68.
*   **REST (Representational State Transfer)**: An **architectural style** or a set of guidelines for designing networked applications, particularly APIs. It emphasizes transferring data accurately in a network.
*   **RESTful API**: A service or an API that **follows the REST principles or guidelines**. REST APIs are often called backend applications and typically fetch data from a database and send responses in JSON format to UI servers.

Q69. **What are the HTTP request and HTTP response structure in the UI and REST API?**
A69.
*   **HTTP Request Structure**: Contains an **HTTP verb (method)** (e.g., `POST`), a **URL**, the **protocol type** (e.g., `HTTP`), the **server address** (UI server or API server), a **request body** (containing data like username/password for `POST` requests, optional for `GET`), and **request headers** (for additional information like content type).
*   **HTTP Response Structure**: Contains a **status code** (indicating success or failure), **content type** (e.g., `JSON`), and the **content itself** (e.g., data in JSON format). The UI server typically converts the JSON response into HTML elements for display in the user's browser.

Q70. **What are the top five REST guidelines and the advantages of them?**
A70. The top five REST guidelines are:
1.  **Separation of Client and Server**: Client (UI) and server (API) implementations must be independent.
    *   *Advantage*: Easier maintenance for both, and a single API can serve multiple UI applications (e.g., Android, iOS, web).
2.  **Stateless APIs**: The API server should not store any information (state) about past HTTP requests from the client; every request is treated as new and fresh.
    *   *Advantage*: Server remains lightweight and simplified, avoiding state management overhead.
3.  **Uniform Interface**: A unique URL must represent a unique service of the API (e.g., `/shoes` URL always gets shoes list).
    *   *Advantage*: Standardized URLs make API resources easy to understand and use.
4.  **Cacheable**: Responses to frequently accessed requests should be cachable to improve response speed and performance.
    *   *Advantage*: Increased performance by caching frequently accessed data.
5.  **Layered System**: The API project should follow a layered architecture (e.g., MVC).
    *   *Advantage*: Promotes modular design, allowing independent handling of modules without impacting others, improving maintainability.

Q71. **What is the difference between REST API and SOAP API?**
A71.
*   **Architecture**: REST is an **architectural style**; SOAP is a **protocol** (Simple Object Access Protocol).
*   **Protocols used**: REST uses only **HTTP/HTTPS**; SOAP can use various protocols like HTTP, SMTP.
*   **Data Formats**: REST uses lightweight formats like **JSON, XML**; SOAP typically uses **XML**.
*   **Statefulness**: REST APIs are **stateless**; SOAP APIs can be stateful or stateless.
*   **Fault Mechanism**: REST relies on **HTTP status codes** (e.g., 200, 404); SOAP defines its own fault mechanism.
*   **Performance**: REST APIs are generally **lightweight and faster**; SOAP APIs can be slower due to XML processing. REST APIs are currently more popular.

Q72. **What are HTTP verbs and HTTP methods?**
A72. **HTTP verbs and HTTP methods are the same things**. They are a set of functions that a client can perform on a resource. These methods (e.g., `GET`, `POST`, `PUT`, `DELETE`, `PATCH`) are sent along with the URL in an HTTP request to indicate the type of action desired (e.g., retrieve data, submit data).

Q73. **What are the GET, POST, PUT and DELETE HTTP methods?**
A73.
*   **GET**: Used to **retrieve data** from a specified resource. The request body is optional.
    *   *Example*: `GET /users` (retrieves a list of all users) or `GET /users/123` (retrieves details of a single user).
*   **POST**: Used to **submit data to be processed** (e.g., creating a new resource). The request body typically contains the data to be sent to the server.
    *   *Example*: `POST /users` with user data in the body (creates a new user).
*   **PUT**: Used to **update a resource or create a new resource if it does not exist**. It typically requires the complete resource data in the request body for full replacement.
    *   *Example*: `PUT /users/123` with complete updated user details in the body (replaces the existing user 123).
*   **DELETE**: Used to **remove a specified resource**. The request body is optional.
    *   *Example*: `DELETE /users/123` (deletes user 123 from the database).

Q74. **What is the difference between the PUT and the PATCH methods?**
A74. Both `PUT` and `PATCH` methods are used to update a resource.
*   **PUT**: Performs a **complete resource replacement**. The request body sent by the client should contain *all* the details of the resource, replacing the existing resource entirely.
*   **PATCH**: Performs a **partial resource update**. The client sends *only those fields that need modification* in the request body, leaving other fields of the resource unchanged.

Q75. **Explain the concept of Idempotent in RESTful API.**
A75. **Idempotent** is a concept that guarantees that **performing the same operation multiple times will always give the same output (same response, same result)**.
*   **Idempotent methods**: `GET`, `PUT`, and `DELETE` are idempotent.
    *   `GET`: Requesting a resource multiple times always returns the same resource list/details.
    *   `PUT`: Updating a resource multiple times with the same data will result in the same final state of the resource.
    *   `DELETE`: Deleting a resource multiple times will result in the resource being deleted (first time) and then subsequent requests will indicate it's no longer found, which is a consistent outcome.
*   **Non-Idempotent methods**: `POST` is non-idempotent. Sending multiple `POST` requests with the same body will typically create a *new* resource each time (e.g., a new user with a new ID), leading to different results.

Q76. **What is the role of Status Codes in RESTful APIs?**
A76. **Status codes are used to convey the results of a client request** to the client from the REST API. They inform the client whether a request was successful, failed, redirected, or if there was an error.
*   **1xx (Informational)**: Response is informational.
*   **2xx (Success)**: Client request was successful on the server (e.g., **200 OK** - successful with content; **204 No Content** - successful but no content in response).
*   **3xx (Redirection)**: Client request was redirected.
*   **4xx (Client Error)**: Client request was rejected or failed due to a client-side problem (e.g., **400 Bad Request** - incorrect request format/data type; **401 Unauthorized** - request not authorized; **403 Forbidden** - authorized but forbidden for specific resource; **404 Not Found** - resource not found).
*   **5xx (Server Error)**: Client request was rejected due to a server-side problem, not the client's fault (e.g., **500 Internal Server Error** - server down, connection issue).

Q77. **What is CORS in RESTful APIs?**
A77. **CORS (Cross-Origin Resource Sharing) is a security feature provided by web browsers** (e.g., Chrome, Edge). By default, CORS policy **restricts web pages from accessing resources (data) from different "origins"** (different websites, subdomains, protocols like HTTP vs HTTPS, or different port numbers). This means a website (e.g., `interview.com`) cannot, by default, directly fetch data from another different website (e.g., `xyz.com`). Developers sometimes need to explicitly allow cross-origin data sharing in their API code.

Q78. **How to remove CORS restriction on RESTful API?**
A78. To remove CORS restriction, you typically use the **`cors` middleware** in your Express.js application.
1.  **Install the `cors` middleware**: `npm install cors` (as it's a third-party module).
2.  **Import it**: `const cors = require('cors');`.
3.  **Enable it for all routes globally**: `app.use(cors());`. This allows any website from any domain to access data from your API.
4.  **To configure CORS (allow specific domains)**: Pass a configuration object to the `cors` middleware, specifying allowed origins (e.g., `app.use(cors({ origin: 'http://example.com' }));`). This removes restrictions only for the specified domain, keeping them for others.

Q79. **What are Serialization and Deserialization?**
A79.
*   **Serialization**: The process of **converting a data object (or data structure) into a format suitable for transmission** over a network or storage (e.g., JSON, binary, bytes).
*   **Deserialization**: The process of **converting data that has been serialized (e.g., JSON string) back into an object** or data structure that can be used by the program.
These processes are essential because different technologies handle objects differently, but common formats like JSON ensure data can be universally understood and exchanged between APIs built in various languages (Java, .NET, Node, etc.).

Q80. **What are the types of Serialization?**
A80. There are mainly three types of serialization:
1.  **Binary Serialization**: Converts data or objects to binary or byte format.
2.  **XML Serialization**: Converts objects to XML format.
3.  **JSON Serialization**: Converts objects or data structures to JSON format. This is the most popular type.

Q81. **How to serialize and deserialize in Node.js?**
A81. Node.js uses the built-in `JSON` object for serialization and deserialization:
*   **Serialization (Object to JSON string)**: Use `JSON.stringify()`. You pass the JavaScript object as an argument, and it returns the converted JSON string.
    *   *Example*: `const jsonString = JSON.stringify(myObject);`.
*   **Deserialization (JSON string to JavaScript object)**: Use `JSON.parse()`. You pass the JSON string as an argument, and it returns the corresponding JavaScript object.
    *   *Example*: `const myObject = JSON.parse(jsonString);`.

Q82. **Explain the concept of Versioning in RESTful APIs.**
A82. **Versioning in RESTful APIs refers to the practice of maintaining multiple versions of an API** over time as new requirements emerge. This is done to **support backward compatibility**. When a new version (e.g., V3) with changes is released, older client applications that are not yet ready to accommodate these changes can continue to use previous versions (e.g., V1, V2) of the API without breaking their functionality. Different URLs or headers are often used to indicate which API version a client wishes to use.

Q83. **What is an API document? What are the popular documentation formats?**
A83. An **API document describes the functionality, features, and usage of a REST API**. It is created and shared with clients (e.g., Android, iOS, web UI application developers) to inform them about the API methods, request structures, and response formats. This helps clients easily integrate with and consume the API services.
Popular documentation formats include:
*   **Swagger / OpenAPI**
*   **RAML**
*   **API Blueprint**

Q84. **What is the typical structure of a REST API project in Node?**
A84. A typical Node.js REST API project often has the following folder and file structure:
*   **`node_modules/`**: Contains npm packages (should not be touched).
*   **`src/` (Source folder)**: Main focus of the project.
    *   **`controllers/`**: Contains files with business logic and endpoint methods (`GET`, `POST`, `PUT`, `DELETE`).
    *   **`models/`**: Contains data models or properties related to the application's entities (e.g., products, users).
    *   **`routes/`**: Contains configuration for the routing system, grouping and nesting related routes (e.g., `productRoutes.js`, `userRoutes.js`).
    *   **`utils/`**: Contains helper methods that can be reused throughout the application (e.g., `errorHandling.js`, `validation.js`).
*   **`app.js`**: The main entry file where requests enter, and middlewares, controllers, and routes are called.
*   **`.gitignore`**: Specifies files/directories to be ignored by version control (e.g., `node_modules/`).
*   **`package.json`**: Contains project metadata and its dependencies.

Q85. **What are Authentication and Authorization?**
A85.
*   **Authentication**: The process of **verifying a user's identity**. It answers the question, "**Who are you?**". This typically involves a user providing credentials (like username and password), which the system then validates against a database to confirm their identity.
*   **Authorization**: The process of **determining what a verified user is allowed to do or access**. It determines "**What are you allowed to do?**". This is based on the user's roles or rights (e.g., a student can view results but not edit them, while a teacher can edit).
**Authentication always happens before Authorization**.

Q86. **What are the types of authentication in Node?**
A86. The five main types of authentication (applicable to almost all technologies, including Node) are:
1.  **Basic Authentication**
2.  **API Key Authentication**
3.  **Token Based Authentication** (JWT authentication is a type of this)
4.  **Multi-factor Authentication**
5.  **Certificate Based Authentication**

Q87. **What is Basic Authentication?**
A87. In **Basic Authentication**, a user logs in with a **username and password** in the UI. These credentials are then passed to the REST API, which validates them against its database to authenticate the user.
*   **Disadvantage**: Username and password are **sent as plain text over the network** (not encrypted/encoded), and passwords might be stored in plain text in the database. This is considered **not a secure method**.

Q88. **What are the security risk associated with storing password as plain text in Node.js?**
A88. Storing passwords as plain text in a database carries significant security risks:
*   **Unauthorized Access**: If a hacker gains access to the database, they can easily use the plain text usernames and passwords to log into user accounts and steal information.
*   **Compromise of Other Accounts**: Many users reuse the same password across multiple accounts (e.g., banking, social media). If a hacker obtains a plain text password from one database, they might be able to access other unrelated accounts belonging to the same user.
For these reasons, passwords should always be stored in an encrypted format using algorithms.

Q89. **What is the role of Hashing and Salt in securing passwords?**
A89. Hashing and salting are used to **secure passwords or confidential information**.
*   **Hashing**: Involves encrypting or encoding a plain text password using a **one-way algorithm** (e.g., SHA-256) to produce an encrypted password. This provides a basic level of security.
*   **Salting**: To add more security, a **random string (salt)** is generated (e.g., using `bcrypt` or `crypto` libraries). This salt is then **combined with the plain text password before hashing**. The unique salt for each password makes it much harder for hackers to use techniques like rainbow tables or brute-force attacks, even if they know the hashing algorithm and the encrypted password, because they won't know the unique salt.

Q90. **How can we create hash passwords in Node.js?**
A90. To create secure hash passwords in Node.js using the `crypto` library:
1.  **Import the `crypto` library**: `const crypto = require('crypto');`.
2.  **Define a function to hash and salt**: This function takes the plain text password.
3.  **Generate a random salt**: Use `crypto.randomBytes()` (e.g., `crypto.randomBytes(16).toString('hex')`).
4.  **Create a hash object**: Specify the algorithm (e.g., `crypto.createHash('sha256')`).
5.  **Combine salt and password into the hash object**: Use the `update()` function (e.g., `hash.update(salt + plainTextPassword)`).
6.  **Convert the hash object to a string**: Use the `digest()` function (e.g., `hash.digest('hex')`) to get the hexadecimal string of the hash.
7.  **Return the complete secure password** (often by combining the salt and the hash string). The salt string can be stored separately from the hash string in the database for even more security.

Q91. **What is API Key Authentication?**
A91. In **API Key Authentication**, the REST API owner or developer **creates a single API key and shares it with all clients/users** of the API. Clients then simply pass this API key in their requests (e.g., in the header) for authentication, instead of usernames and passwords.
*   **Benefit**: Simple management as there's only one key, no need to store multiple usernames/passwords in the database.
*   **Disadvantage**: The API key can be very easily shared by clients, allowing unwanted clients to access the API, making it less secure than other methods.

Q92. **What is Token Based Authentication and JWT Authentication?**
A92.
*   **Token Based Authentication**: A type of authentication where **tokens are used instead of traditional credentials** (username/password) for subsequent requests after initial authentication.
*   **JWT (JSON Web Token) Authentication**: A **specific type of token-based authentication** where JWTs are used as the tokens.
**JWT Authentication Process (8 steps)**:
1.  **User sends username and password** from the client/browser to the API with a `POST` request.
2.  **API receives and validates** these credentials.
3.  If valid, **API creates a JWT token** and sends it back to the client as a response. If invalid, an authentication error is returned.
4.  **Client stores this JWT token** (e.g., in local storage or cookies of the browser).
5.  For every future request for data, the **client sends this JWT token in the header** of the request to the API.
6.  **API receives the token** and validates its signature using an algorithm.
7.  If the **token is valid**, the API sends the requested data to the client.
8.  **Client displays the data** in the browser.
This process ensures that username/password are sent only once, and subsequent requests are authenticated via the token, improving security and efficiency.

Q93. **What are the parts of the JWT token?**
A93. A JWT token is a string **separated by dots into three parts**:
1.  **Header**: Consists of the **type of token** (e.g., JWT) and the **algorithm used** to generate the token (e.g., HS256).
2.  **Payload**: Contains the **claims**, which are pieces of information about the token. This includes issuer, subject (typically identifying the user), expiration time, and issue time.
3.  **Signature**: The **most important part** for verification. It is created by encoding the header and the payload of the token using a secret key. When the REST API receives the token, it verifies the signature to ensure the token's validity and integrity.

Q94. **Where JWT token resides in the request?**
A94. The JWT token typically resides **inside the request header**, specifically within the `Authorization` header. The value usually starts with "Bearer " followed by the actual token string.

Q95. **What is error handling? How many ways you can implement error handling in Node applications?**
A95. **Error handling is the process of managing errors that occur during the execution of a program or application**. This involves capturing, logging, and properly responding to errors, and then analyzing them for fixes.
Four common techniques for error handling in Node.js are:
1.  **Try-catch block** (for synchronous operations).
2.  **Error-first callbacks** (for asynchronous operations).
3.  **Promises** (with `.catch()` for asynchronous operations).
4.  **Try-catch with async/await** (for asynchronous operations).

Q96. **How to handle errors in synchronous operations using try-catch-finally?**
A96.
*   **Try block**: All synchronous code where errors might occur is placed inside the `try` block.
*   **Catch block**: If any error occurs within the `try` block, execution immediately transfers to the `catch` block. The `catch` block receives the error object as a parameter, allowing developers to log error details and send appropriate responses.
*   **Finally block**: Code placed inside the `finally` block will **always execute**, regardless of whether an error occurred in the `try` block or was caught in the `catch` block. This is useful for cleanup operations (e.g., closing connections) that must run in all scenarios.

Q97. **What is Error First Callbacks?**
A97. **Error First Callbacks are a way of handling errors in asynchronous operations** in Node.js. The naming signifies their structure: the **first parameter of the callback function is always reserved for an error object**. If an error occurs during an asynchronous operation, that error object is passed as the first argument to the callback; otherwise, it's typically `null` or `undefined`. This allows the callback function to handle errors in a consistent and structured manner.

Q98. **How to handle errors using Promises?**
A98. When using Promises for asynchronous operations, errors are handled primarily with the **`.catch()` block**. If an operation inside a Promise fails, the Promise `reject`s, and the error passed during rejection is then received and processed by the subsequent `.catch()` block in the Promise chain.

Q99. **How to handle errors using async/await?**
A99. When using `async/await` for asynchronous operations, errors are handled using the **`try-catch` block**. The code that performs the asynchronous operation (which returns a Promise and is `await`ed) is placed inside the `try` block. If the awaited Promise rejects (an error occurs), the control is immediately transferred to the `catch` block, where the error can be handled.

Q100. **How can you debug Node.js application?**
A100. Five techniques to debug Node.js applications are:
1.  **`console.log()`**: Using `console.log()` statements to print variable values and execution flow.
2.  **`debugger` statement**: Inserting the `debugger` keyword in code to trigger a breakpoint when Node.js is run with debugging enabled.
3.  **Node.js Inspector Tools**: Using Node.js's built-in debugging client or connecting external debuggers.
4.  **Visual Studio Code Debugger**: Utilizing the integrated debugger within VS Code.
5.  **Chrome Developer Tools**: Using the Chrome browser's developer tools for debugging, as Node.js runs on the V8 engine.

---

### Summary Table of All Questions

| Q.No. | Question |
| :---- | :------------------------------------------------------------------------------------------------ |
| Q1    | What is Node.js?                                                                                  |
| Q2    | What is the difference between a framework and a runtime environment?                              |
| Q3    | What is the difference between Node.js and Express.js?                                            |
| Q4    | What are the differences between client-side and server-side?                                     |
| Q5    | What are the seven main features of Node?                                                         |
| Q6    | What is single-threaded programming?                                                              |
| Q7    | What is synchronous programming?                                                                  |
| Q8    | What is multi-threaded programming?                                                               |
| Q9    | What is asynchronous programming?                                                                 |
| Q10   | What is the difference between synchronous and asynchronous programming?                          |
| Q11   | What are events, event emitter, event Q, event Loop, and event driven in Node?                    |
| Q12   | What are the main features and advantages of Node?                                                |
| Q13   | What are the disadvantages of Node? When to use or when not to use Node?                          |
| Q14   | How to set up a Node project?                                                                     |
| Q15   | What is npm? What is the role of Node modules folder in your project?                             |
| Q16   | What are Node modules?                                                                            |
| Q17   | What is the role of package.json file in Node?                                                    |
| Q18   | What are modules in Node? What is the difference between a function and a module?                 |
| Q19   | How many ways are there to export a module?                                                       |
| Q20   | What will happen if you do not export the module?                                                 |
| Q21   | How to import single or multiple functions from a module?                                         |
| Q22   | What is module wrapper function?                                                                  |
| Q23   | What are the types of modules in Node?                                                            |
| Q24   | What are the top five built-in modules commonly used in Node projects?                            |
| Q25   | Explain the role of the FS module. Name some functions of it.                                     |
| Q26   | Explain the role of the Path module. Name some functions of it.                                   |
| Q27   | Explain the role of the OS module. Name some functions of it.                                     |
| Q28   | Explain the role of Events module. How to handle events in Node?                                  |
| Q29   | What are event arguments?                                                                         |
| Q30   | What is the difference between a function and an event?                                           |
| Q31   | What is the role of HTTP module in Node?                                                          |
| Q32   | What is the role of `createServer` method of the HTTP module?                                     |
| Q33   | What are the advantages of using Express with Node?                                               |
| Q34   | How do you install Express in a Node project?                                                     |
| Q35   | How to create an HTTP server using Express.js?                                                    |
| Q36   | How do you create and start the Express application?                                              |
| Q37   | What is middleware in Express.js and when to use them?                                            |
| Q38   | How to implement middleware in Express?                                                           |
| Q39   | What is the purpose of the `app.use` function in Express?                                         |
| Q40   | What is the purpose of the `next` parameter in Express.js?                                        |
| Q41   | How to use middleware globally for a specific route?                                              |
| Q42   | What is the request pipeline in Express?                                                          |
| Q43   | What are the types of middlewares in Express.js?                                                  |
| Q44   | What is the difference between Application Level and Router level middleware?                     |
| Q45   | What is error handling middleware and how to implement it?                                        |
| Q46   | If you have five middlewares then in which middleware you will do the error handling?             |
| Q47   | What is built-in middleware? How to serve static files from the Express.js?                       |
| Q48   | What are third-party middleware? Give some examples.                                              |
| Q49   | Can you summarise all the types of middlewares?                                                   |
| Q50   | What are the advantages of using middlewares in Express.js?                                       |
| Q51   | What is routing in Express?                                                                       |
| Q52   | What is the difference between middleware and routing in Express?                                 |
| Q53   | How to implement routing? How do you define routes in Express?                                    |
| Q54   | How to handle routing in Express real applications?                                               |
| Q55   | What are route handlers?                                                                          |
| Q56   | What are route parameters in Express?                                                             |
| Q57   | What are router object and router methods and how to implement them?                              |
| Q58   | What are the types of router methods?                                                             |
| Q59   | What is the difference between `app.get` and `router.get` methods?                                |
| Q60   | What is `express.Router` in Express.js?                                                           |
| Q61   | Share a real application use of routing.                                                          |
| Q62   | What is route chaining in Express?                                                                |
| Q63   | What is route nesting in Express?                                                                 |
| Q64   | How to implement route nesting in Express?                                                        |
| Q65   | What are template engines in Express?                                                             |
| Q66   | Name some template engine libraries.                                                              |
| Q67   | How to implement EJS templating engine in Express application?                                    |
| Q68   | What are REST and RESTful API?                                                                    |
| Q69   | What are the HTTP request and HTTP response structure in the UI and REST API?                     |
| Q70   | What are the top five REST guidelines and the advantages of them?                                 |
| Q71   | What is the difference between REST API and SOAP API?                                             |
| Q72   | What are HTTP verbs and HTTP methods?                                                             |
| Q73   | What are the GET, POST, PUT and DELETE HTTP methods?                                              |
| Q74   | What is the difference between the PUT and the PATCH methods?                                     |
| Q75   | Explain the concept of Idempotent in RESTful API.                                                 |
| Q76   | What is the role of Status Codes in RESTful APIs?                                                 |
| Q77   | What is CORS in RESTful APIs?                                                                     |
| Q78   | How to remove CORS restriction on RESTful API?                                                    |
| Q79   | What are Serialization and Deserialization?                                                       |
| Q80   | What are the types of Serialization?                                                              |
| Q81   | How to serialize and deserialize in Node.js?                                                      |
| Q82   | Explain the concept of Versioning in RESTful APIs.                                                |
| Q83   | What is an API document? What are the popular documentation formats?                               |
| Q84   | What is the typical structure of a REST API project in Node?                                      |
| Q85   | What are Authentication and Authorization?                                                        |
| Q86   | What are the types of authentication in Node?                                                     |
| Q87   | What is Basic Authentication?                                                                     |
| Q88   | What are the security risk associated with storing password as plain text in Node.js?             |
| Q89   | What is the role of Hashing and Salt in securing passwords?                                       |
| Q90   | How can we create hash passwords in Node.js?                                                      |
| Q91   | What is API Key Authentication?                                                                   |
| Q92   | What is Token Based Authentication and JWT Authentication?                                        |
| Q93   | What are the parts of the JWT token?                                                              |
| Q94   | Where JWT token resides in the request?                                                           |
| Q95   | What is error handling? How many ways you can implement error handling in Node applications?      |
| Q96   | How to handle errors in synchronous operations using try-catch-finally?                           |
| Q97   | What is Error First Callbacks?                                                                    |
| Q98   | How to handle errors using Promises?                                                              |
| Q99   | How to handle errors using async/await?                                                           |
| Q100  | How can you debug Node.js application?                                                            |

### Top 20 List of “Most Important for Beginners” Questions

These questions cover fundamental concepts and essential practical knowledge for anyone starting with Node.js and Express.js, as highlighted in the source:

1.  **What is Node.js?**
2.  **What is the difference between a framework and a runtime environment?**
3.  **What is the difference between Node.js and Express.js?**
4.  **What are the differences between client-side and server-side?**
5.  **What are the seven main features of Node?**
6.  **What is asynchronous programming?**
7.  **What are events, event emitter, event Q, event Loop, and event driven in Node?**
8.  **What are the main features and advantages of Node?**
9.  **What are the disadvantages of Node? When to use or when not to use Node?**
10. **What is npm? What is the role of Node modules folder in your project?**
11. **What are modules in Node? What is the difference between a function and a module?**
12. **What are the types of modules in Node?**
13. **What are the top five built-in modules commonly used in Node projects?**
14. **Explain the role of the FS module. Name some functions of it.**
15. **Explain the role of the HTTP module in Node?**
16. **What are the advantages of using Express with Node?**
17. **What is middleware in Express.js and when to use them?**
18. **What is the purpose of the `next` parameter in Express.js?**
19. **What are REST and RESTful API?**
20. **What are Authentication and Authorization?**

### Top 20 List of “Most Common in Real Interviews”

These questions are frequently encountered in Node.js developer interviews, often testing both theoretical understanding and practical application scenarios:

1.  **What is Node.js?**
2.  **What are the seven main features of Node?**
3.  **What are the main features and advantages of Node?**
4.  **What are the disadvantages of Node? When to use or when not to use Node?**
5.  **What are the top five built-in modules commonly used in Node projects?**
6.  **What is middleware in Express.js and when to use them?**
7.  **What is the purpose of the `next` parameter in Express.js?**
8.  **What is error handling middleware and how to implement it?**
9.  **If you have five middlewares then in which middleware you will do the error handling?**
10. **What are third-party middleware? Give some examples.**
11. **What is routing in Express?**
12. **What is the difference between middleware and routing in Express?**
13. **What is the difference between `app.get` and `router.get` methods?**
14. **What are REST and RESTful API?**
15. **What are the top five REST guidelines and the advantages of them?**
16. **What is CORS in RESTful APIs?**
17. **What are Serialization and Deserialization?**
18. **What are Authentication and Authorization?**
19. **What is Token Based Authentication and JWT Authentication?**
20. **What is error handling? How many ways you can implement error handling in Node applications?**
