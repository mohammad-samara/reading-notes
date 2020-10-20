# Authentication + Role Based Authorization

## RBAC

In computer systems security, role-based access control or role-based security is an approach to restricting system access to authorized users. It is used by the majority of enterprises with more than 500 employees, and can implement mandatory access control or discretionary access control.

Role-based access control (RBAC) restricts network access based on a person's role within an organization and has become one of the main methods for advanced access control. The roles in RBAC refer to the levels of access that employees have to the network.

### BENEFITS OF RBAC

Managing and auditing network access is essential to information security. Access can and should be granted on a need-to-know basis. With hundreds or thousands of employees, security is more easily maintained by limiting unnecessary access to sensitive information based on each user’s established role within the organization.

1. Reducing administrative work and IT support.
2. Maximizing operational efficiency
3. Improving compliance.

### BEST PRACTICES FOR IMPLEMENTING RBAC

* Current Status: Create a list of every software, hardware and app that has some sort of security.
* Current Roles: Even if you do not have a formal roster and list of roles, determining what each individual team member does may only take a little discussion. Try to organize the team in such a way that it doesn’t stifle creativity and the current culture
* Write a Policy: Any changes made need to be written for all current and future employees to see. Even with the use of a RBAC tool, a document clearly articulating your new system will help avoid potential issues.
* Make Changes: Once the current security status and roles are understood (not to mention a policy is written), it’s time to make the changes.
* Continually Adapt: It’s likely that the first iteration of RBAC will require some tweaking. Early on, you should evaluate your roles and security status frequently. Assess first, how well the creative/production process is working and secondly, how secure your process happens to be.

## React Cookies

Install it with `npm i react-cookies`

* Then import it and save it as a state by `cookie.load('token')`

```Javascript
// The div only shows if you are logged in
  <Auth>
    <div />
  </Auth>

  // The div only shows if you are logged in AND have read permissions
  <Auth capability="read">
    <div />
  </Auth>
```
