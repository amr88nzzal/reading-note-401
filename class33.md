# `<Login />` and `<Auth />`

### 1. Why is the Context API useful?
- The React Context API is a way for a React app to effectively produce global variables that can be passed around. This is the alternative to "prop drilling" or **moving props from grandparent to child to parent, and so on**. **Context is also touted as an easier, lighter approach to state management using Redux.**
    - Context is designed to share data that can be considered “global” for a tree of React components

### 2. Can a component outside of a provider get its context?
- No, it's can't.
### 3. What are some common use cases for using the Context API?
- Theming — Pass down app theme. i18n — Pass down translation messages. Authentication — Pass down current authenticated user.

### 4. Describe “Context Hell”.
- The React Context hell is the nasty code you get taking advantage of the React Context API (Providers inside Providers ...). 

*** 
## Vocabulary Terms: 
| Term      | Definition                                                                                                 |
| --------- | ---------------------------------------------------------------------------------------------------------------|
| global state|state that is accessible at the top level of the app and passed via props.|
| global context| Context provides a way to share values and data between components without having to explicity pass a prop through every level of the tree. Designed to share data that can be considered "global" for a tree of React components, such as the current authenticated user, theme, or preferred language. |
| provider|The component that is sharing context to child components  |
| consumer| The components that use the context given to them by a parent component  |
*** 
 
## Preparation Materials:
 
  #### what is role based access control?
- Role-based access control (RBAC) restricts network access based on a person's role within an organization and has become one of the main methods for advanced access control. The roles in RBAC refer to the levels of access that employees have to the network.

- An employee's role in an organization determines the permissions that individual is granted and ensures that lower-level employees can't access sensitive information or perform high-level tasks.

- In the role-based access control data model, roles are based on several factors, including authorization, responsibility and job competency. As such, companies can designate whether a user is an end user, an administrator or a specialist user. In addition, access to computer resources can be limited to specific tasks, such as the ability to view, create or modify files.

- Limiting network access is important for organizations that have many workers, employ contractors or permit access to third parties, like customers and vendors, making it difficult to monitor network access effectively. Companies that depend on RBAC are better able to secure their sensitive data and critical applications.

  #### EXAMPLES OF ROLE-BASED ACCESS CONTROL
Through RBAC, you can control what end-users can do at both broad and granular levels. You can designate whether the user is an administrator, a specialist user, or an end-user, and align roles and access permissions with your employees’ positions in the organization. Permissions are allocated only with enough access as needed for employees to do their jobs.

### Some of the designations in an RBAC tool can include:
- Management role scope – it limits what objects the role group is allowed to manage.
- Management role group – you can add and remove members.
- Management role – these are the types of tasks that can be performed by a specific role group.
- Management role assignment – this links a role to a role group.

## Benefits of RBAC
- Managing and auditing network access is essential to information security.

There are a number of benefits to using RBAC to restrict unnecessary network access based on people's roles within an organization, including:

1. **Reducing administrative work and IT support**. With RBAC, you can reduce the need for paperwork and password changes when an employee is hired or changes their role. Instead, you can use RBAC to add and switch roles quickly and implement them globally across operating systems, platforms and applications. **It also reduces the potential for error when assigning user permissions.** This reduction in time spent on administrative tasks is just one of several economic benefits of RBAC. RBAC also helps to more easily integrate third-party users into your network by giving them pre-defined roles.
   
2. **Maximizing operational efficiency.** RBAC offers a streamlined approach that is logical in definition. Instead of trying to administer lower-level access control, all the roles can be aligned with the organizational structure of the business and users can do their jobs more efficiently and autonomously.
   
3. **Improving compliance.** All organizations are subject to federal, state and local regulations. With an RBAC system in place, companies can more easily meet statutory and regulatory requirements for privacy and confidentiality as IT departments and executives have the ability to manage how data is being accessed and used. 
   

#### Best practices for role-based access control implementations

There are a number of best practices organizations should follow for implementing RBAC, including:

- **Current Status:** Create a list of every software, hardware and app that has some sort of security. For most of these things, it will be a password. However, you may also want to list server rooms that are under lock and key. Physical security can be a vital part of data protection. Also, list the status of who has access to all of these programs and areas. This will give you a snapshot of your current data scenario.

- **Current Roles:** Even if you do not have a formal roster and list of roles, determining what each individual team member does may only take a little discussion. Try to organize the team in such a way that it doesn’t stifle creativity and the current culture (if enjoyed).

- **Write a Policy:** Any changes made need to be written for all current and future employees to see. Even with the use of a RBAC tool, a document clearly articulating your new system will help avoid potential issues.

- **Make Changes:** Once the current security status and roles are understood (not to mention a policy is written), it’s time to make the changes.

- **Continually Adapt:** It’s likely that the first iteration of RBAC will require some tweaking. Early on, you should evaluate your roles and security status frequently. Assess first, how well the creative/production process is working and secondly, how secure your process happens to be.


#### react-cookies component
- HTTP cookies, or internet cookies, are built specifically for Internet web browsers to track, personalize, and save information about each user's session. A “session” just refers to the time you spend on a site. Cookies are created to identify you when you visit a new website.
  

- react-cookies is a Load and save cookies with React

Install
 `npm install react-cookies --save`

 *** 
