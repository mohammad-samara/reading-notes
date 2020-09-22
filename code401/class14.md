# Access Control (ACL)

## Access Controls

- Access Controls are the selective restriction of resources. Access Controls are implemented everywhere in computer systems.
- In RESTful APIs, it is important to limit access to clients based on credentials. This means a user (Foo) should not be able to delete a users (Bar) resource, unless Bar said that Foo is allowed to. Limiting what actions a user can preform on a given resource is called Access Control. A user can be given a token at signup and login, and that user can pass that token back to the server on requests with limited access controls. Once the server parses the token, it can determine if the user is authorized to preform the request.

### Application Flow and Access Control

- Applications of all types have varying degrees of access based on user type and UI requirements.  
**A CMS might:**

- Allow admin users to create categories, content, manage user accounts, and run reports
- Allow editor users to create, edit and delete existing content, but not see or manage user accounts
- Allow guest users to access (read) content
- Allow user users (logged in users) to access (read) content and apply a thumbs-up/down to content, but not change the actual content

### What is RBAC?(Role-based access control)

idea of assigning system access to users based on their role within an organization.

### Benefits of RBAC

With the proper implementation of RBAC, the assignment of access rights becomes systematic and repeatable. Further, it is much easier to audit user rights, and to correct any issues identified.  
  
RBAC may sound intimidating, but it can in reality be easy to implement, and will make the ongoing management of access rights much easier and more secure.  
  
The data breach you prevent may be your own.
