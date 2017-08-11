# Using cloudscribe Core with IdentityServer4 and Entity Framework Core - MySql

cloudscribe Core and IdentityServer4 integration provides a compelling solution that makes it easy to provision new OP (OpenId Connect Provider) Servers each with their own Users, Roles, Claims, Clients, and Scopes. It includes a UI for managing all the needed data including role and claim assignments for users.

This sample provides a ready to run multi-tenant OP (OpenId Connect Provider) Server. On the first run it will initialize the database and create an admin user with the credentials admin@admin.com and the password "admin".

Once you login an Administration Menu will appear providing links to all the management features for tenants, user, roles, calims, clients, and scopes.

Note that you do not have to use the multi-tenancy features, it works just as well in a single tenant scenario.

Due to a known issue, the migrations won't work if you set the connection string to an existing MySql database. However, if you use a database name that does not exist and a user with sufficient permission to create a database, then it will create a database and migrations will work. After that you can change the connection string to a less priviledged user.


## Meta

This sample uses [cloudscribe Core](https://github.com/joeaudette/cloudscribe) for user authentication and Entity Framework Core for data storage.

[cloudscribe Core](https://github.com/joeaudette/cloudscribe) is a multi-tenant web application foundation. It provides multi-tenant identity management for sites, users, and roles.

This sample is using a fork of [IdentityServer4](https://github.com/joeaudette/IdentityServer4) with minimal changes that were needed to support folder tenants of the OP Server. I am hoping to get changes into the main IdentityServer4 to support this scenario, this fork is hopefully a temporary solution.

[![Join the chat at https://gitter.im/joeaudette/cloudscribe](https://badges.gitter.im/joeaudette/cloudscribe.svg)](https://gitter.im/joeaudette/cloudscribe?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge)




