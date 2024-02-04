# Maintainer's manual documentation

Welcome to the Comprehensive Maintainer's Manual for the Assignment Calculator App. This manual serves as a detailed guide for individuals responsible for maintaining, enhancing, and troubleshooting the Assignment Calculator, an innovative application designed to facilitate effective assignment management for students.

### Purpose of the Manual
The primary objective of this manual is to provide maintainers with a comprehensive understanding of the Assignment Calculator's system design, test facilities, and deployment procedures. By offering detailed insights into the application's architecture, testing methodologies, and deployment strategies, this document aims to empower maintainers to efficiently manage, update, and optimize the Assignment Calculator.

### Overview of the Assignment Calculator App
The Assignment Calculator is a user-friendly tool that assists students in breaking down assignments into manageable subtasks, helping them organize their work and meet deadlines. This application is built with a focus on usability, scalability, and maintainability, ensuring a smooth user experience for both students and administrators.

### In this article
1. [System Design](#system-design)
2. [Deployment](#deployment)

## System Design
This section delves into the architecture and design principles that form the foundation of the Assignment Calculator. It covers aspects such as data flow, component interactions, and external dependencies, providing maintainers with a comprehensive understanding of the system's structure.

### Main Functions
1. The process of creating subtasks within the Assignment Calculator is facilitated by the **Step** class, a pivotal component in the application's architecture. This class, as defined in the provided [source code](https://github.com/HuuDatDo/Softcon/blob/main/Assignment-Calculator.html#L1591), is equipped with an initialization function that sets essential parameters such as the start date, due date, and ISO suffix. The meticulous design of the **Step** class allows for precise control over these temporal elements, ensuring accurate computation of deadlines for individual subtasks.

2. The functionality of the **Step** class extends beyond mere initialization, as evidenced by the array of [methods](https://github.com/HuuDatDo/Softcon/blob/main/Assignment-Calculator.html#L1608) it offers. Notably, these methods play a crucial role in calculating the total number of available days for an assignment. By leveraging intricate algorithms and logical operations, the Step class dynamically computes the temporal constraints imposed by the assignment's start and due dates. Subsequently, it employs this information to derive the due date for each subtask, optimizing the distribution of workload across the assignment timeline.

3. Within the intricate design of the Assignment Calculator, another [Vue class](https://github.com/HuuDatDo/Softcon/blob/main/Assignment-Calculator.html#L1669) plays a pivotal role. Responsible for managing user interactions, this class serves as a conduit between the user interface and underlying functionalities, invoking methods for output data generation based on user actions. Beyond interaction management, the Vue class integrates external services, exemplified by a [method](https://github.com/HuuDatDo/Softcon/blob/main/Assignment-Calculator.html#L1696) using the EmailJS API to facilitate email communication.

### Modification on contents
The [content](https://github.com/HuuDatDo/Softcon/blob/main/Assignment-Calculator.html#L500) of each subtask is hardcoded. So developer can edit right in each step.

To add more assignment types, developer can easily specify new [objects](https://github.com/HuuDatDo/Softcon/blob/main/Assignment-Calculator.html#L500) for subtasks, specifying the order via *step* variable and how much they should spend on the subtask via *percentage* variable. Then, they can follow the [template](https://github.com/HuuDatDo/Softcon/blob/main/Assignment-Calculator.html#L282) to finalize the new assignment. 

## Deployment

We provide an open-source front-end with integrated Vue.js functions. For deployment, the procedure will depend on the domain or server, please refer to this [guide](https://docs.github.com/en/pages/getting-started-with-github-pages/creating-a-github-pages-site) for an easy deployment on GitHub pages.