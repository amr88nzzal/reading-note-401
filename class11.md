# Event Driven Applications

## 1. Why is access control important?

 **because it's a valuble security techniqe limiting the access to information, and information processing system, and regulate who or what can use or view any given resource.**

## 2. Describe an application that would need access control.

    - PINs and one-time passwords (OTPs).
    - Login credentials( username & password)

## 3. What is a role used for?

 **A role is a collection of permissions that can be divided to the users according to his tag.**

## 4. Why is role based access control more scalable than discretionary or mandatory access control?

 **The assignment of access rights in RBAC is very systematic and repeatable, easier to audit user rights (users are in only one of a few categories), and easier to correct any issues that are identified. There is no case by case assignment of roles, users fall into one of already pre-assigned roles/capabilities.**
****
## Vocabulary Terms

| Term                       | Definition                                                                                                                                                                                     |
| ------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Authorization             | The function of specifying access rights/privileges to resources, which is related to general information security and computer security, and to access control in particular               |
| Role Based Access Control | (RBAC), A method of restricting network access based on the roles of individual users within an enterprise.                                                        |
| Capabilities              | A set of functions that that the authorized user has access to (like; Read-Update-Write and Delete)  |
****

## Preview

### 1. Which 3 things had you heard about previously and now have better clarity on?

* O-auth
* Middle Wares
* Basic Sign-in

### 2. Which 3 things are you hoping to learn more about in the upcoming lecture/demo?

* Blockchain
* End-to-end encryption (E2EE)
* Event Driven application

### 3. What are you most excited about trying to implement or see how it works?

* encryption

****

## Preparation Materials

### What is Event-Driven Programming? 

it is a logical pattern that we can choose to confine our programming within to avoid issues of complexity and collision.

### Node docs: 

- All objects that emit events are instances of the `EventEmitter` class.
- These objects expose an `eventEmitter.on()` function that allows one or more functions to be attached to named events emitted by the object.
- When the `EventEmitter` object emits an event, all of the functions attached to that specific event are called synchronously, any values returned by the called listeners are ignored and discarded.
- `eventEmitter.on()` is used to register listeners.
- `eventEmitter.emit())` is used to trigger the event.
- The `eventEmitter.emit()` method allows an arbitrary set of arguments to be passed to the listener functions.
****
