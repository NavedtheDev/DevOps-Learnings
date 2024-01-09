# IAM #

* AWS Identity and Access Management (IAM) is a service that enables secure management of access to AWS resources.

* It allows users to define and control permissions, create and manage users, groups, and roles, enhancing security and facilitating fine-grained access control within the AWS environment.

It is mainly for two purposes: <b>Authentication</b> and <b>Authorization</b>



We have 4 main terms here:

1. <b>Users:</b> IAM users are individual entities with unique credentials within an AWS account. They are assigned policies defining their permissions, allowing them to interact with AWS resources.

2. <b>Policies:</b> IAM policies are documents defining permissions and access control rules. They specify what actions are allowed or denied on AWS resources for users, groups, or roles. Policies are attached to these entities to regulate their access, providing a granular and secure way to manage permissions within the AWS environment. If we attach no policies, the user will not be able to do anything except logging in.

3. <b>Groups:</b> A group is a collection of IAM users. Instead of attaching policies directly to individual users, you can create a group, attach policies to the group, and then add users to the group. This helps in managing and assigning permissions at scale, making it more efficient to handle access control.

4. <b>Roles:</b> A role is another entity that you can create and manage. However, unlike groups or users, roles are not associated with a specific AWS identity, such as a user or a group. Instead, roles define a set of permissions for making AWS service requests and are assumed by AWS resources or users outside of your AWS account.
