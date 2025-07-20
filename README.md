# AWS-IAM
### This project will demonstrate how to create IAM in AWS.

### AWS IAM (Identity and Access Management) is a web service that allows you to manage access to AWS resources securely. It enables you to control who can access which AWS services and resources, and under what conditions. Essentially, IAM helps you manage users, security credentials (like access keys), and permissions to control access to your AWS environment.

## Benefits of IAM

### Centralized Management:
IAM allows you to centrally manage users, groups, roles, and permissions within your AWS account. 
### Authentication and Authorization:
It handles authentication (verifying who you are) and authorization (determining what you're allowed to do). 
### Fine-grained Access Control:
IAM enables you to grant very specific permissions, allowing users to access only the resources they need and nothing more. 
### No Additional Charge:
IAM is a core AWS service and is offered at no additional cost. 
### Key Concepts in IAM:
* Users: Individual accounts with permissions to access AWS resources. 
* Groups: Collections of users that share the same permissions. 
* Roles: Entities that can be assumed by trusted identities (users or applications) to grant them temporary permissions. 
* Policies: Documents that define permissions. They specify what actions a user, group, or role is allowed to perform on which AWS resources. 

## Project setup.

* Headover to your AWS acount

![](./img/Pasted%20image.png)

* Navigate to IAM, you do so by using the search bar. Type 'iam' and enter to search.

![](./img/Pasted%20image%20(2).png)


### Create IAM Users.

#### We will create a policy, create group and associate this policy with the group(role based), then create users and add the users to the groups.The policies will be for developer and data analyst groups respectively.

### Create policy for developers group.

* On the IAM page click on 'policies' to begin creating a new policy.

![](./img/Pasted%20image%20(4).png)

* On the policies page, click 'create policy', top right. Search for EC2 and check 'All EC2 actions (ec2:*)'. Recall that developers will need access to EC2 instance in this case.

![](./img/Pasted%20image%20(5).png)

* Scroll down to 'Resources' and select 'All' radio button then click 'next'

![](./img/Pasted%20image%20(6).png)

* Add a policy name 'devlopers'. Add a description if you want.

![](./img/Pasted%20image%20(7).png)

* Scroll down the page and click 'Create policy'

![](./img/Pasted%20image%20(8).png)

* You should a success page as below.

![](./img/Pasted%20image%20(9).png)

### Create policy for data analyst group.

* On the policies page click 'Create policy'

![](./img/Pasted%20image%20(4).png)

* Click 'Select a service' drop down and select S3 service. Check the 'All S3 action' box.

![](./img/Pasted%20image%20(10).png)

* Scroll down click 'All' resources button and click 'next'

![](./img/Pasted%20image%20(11).png)

* Add a policy name 'analyst'. Provide a description(optional) and click 'create policy'

![](./img/Pasted%20image%20(12).png)

* You should see a success page indicating the policy creation was a success.

![](./img/Pasted%20image%20(13).png)



* Head over to the IAM page in your AWS account if not already. You find this page by using the AWS GUI search bar as shown above. Click 'Create user' at the top right.

![](./img/Pasted%20image%20(3).png)

