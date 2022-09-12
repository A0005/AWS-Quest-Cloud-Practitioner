1 - AWS IAM:

    AWS Identity and Access Management (AWS IAM) enables you to manage access to 
    AWS services and resources securely. AWS IAM is a feature of your AWS account
    offered at no additional charge. You will be charged only for use of other 
    AWS services by your users.
    
    Often a collection of users will rewuire a similar set of permissions.
    In order to define permissions for multiple users, an AWS IAM group
    can be used. AWS IAM users can be added to a group and they inherit
    all the permissions that have be attached to the group.
    
    A user group can contain many users, and a user can be belong to multiple
    user groups. User groups can't be nested; they can contain only users, not other
    user groups. There is no default user group that automatically includes all users
    in the AWS account. If you want to have a user a user group like that, you must
    create it and assign each new user to it.
    
    A policy is an object in AWS that, when associated with an identity or
    resource, defines their permissions. AWS evaluates policies every time
    and AWS IAM principal (user or role) makes a request.
    
    AN AWS Identity and Access Management user is an entity that you create in AWS 
    to rrepresent the person or application that uses it to interact with AWS.
    A user in AWS consits of a name and credentials. An AWS IAM user with administrator 
    permissions is not the same thing as the AWS account root user.
    
    Disabling the AWS Management Console access password for a user prevents
    them from signing in the to the AWS Management Console using their user name
    and password. It does not change their permissions or prevent them from
    accessing the console using an assumed role.
    
    A user can belong to more than one group. In the event that groups have 
    conflicting policies AWS has a policy evaluation logic.
    
    Users can have tags associated with them. This can help you manage a 
    large amount of users in the future.
    
    For extra security, enable multi-factor authentication (MFA) for all
    users in your account. with MFA, users have a device that generates a 
    response to an authentication challenge. If the user's password or access keys
    are compromised, your account resources are still secure because of the additional 
    authentication requirement.
    
    The secret access key is available for download only when you create it.
    If you don't download your secret access key or if you lose it, you must create a
    new one. Remember to keep it secret and keep it safe.
    
    As an administrator, you can sign in as your newly created user to review their
    access level. Change your own passwords and access keys regularly, and make sure all
    AWS IAm users in your account do so as well. If you allow users to change their own
    passwords, create a custom password policy that requires them to create strong passwords.
    
    All updates to user and group permissions are instantaneous.
    
    Users can only perform actions that are allowed by the assigned
    AWS IAM policies.
    
2 - Amazon EC2:

    Amazon Elastic Compute Cloud (Amazon EC2) is a web service that
    providesressizable compute capacity in the cloud. It is designed 
    to make web-scale computing easier for developers.
    
    
    Amazon EC2 Dashboard displays meterics on the number of resources by type.
    
    
    
    
    
    
    
    
    
    
    
    
    
