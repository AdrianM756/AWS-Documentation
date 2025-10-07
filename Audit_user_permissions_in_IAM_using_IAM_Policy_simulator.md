## Audit user permissions in IAM using IAM Policy simulator
<br>

AWS Identity and Access Management (IAM) enables you to securely control access to AWS services and resources for your users. Using IAM, you can create and manage AWS users and groups and use permissions to allow and deny their access to AWS resources.
<br>

At the top of the AWS Management Console, in the search bar, search for and choose iam.

<img width="848" height="218" alt="image" src="https://github.com/user-attachments/assets/7b44228c-ff48-49fa-a46a-dbeff8a00815" />
<br>

In the navigation panel at the left of the page, under ```Access management```, choose ```Users```.

<img width="254" height="389" alt="image" src="https://github.com/user-attachments/assets/fd79276c-2500-45a4-9c65-1d9a7b71fe91" />
<br>

On the ```Users``` page, choose the link for ```user-1``` to view its details and review the ```Summary``` section for information about your user. Select the ```Security credentials``` tab to review it. Here, you can see how many access keys a user has, when an access key was created, whether a Multi-Factor Authentication (MFA) device is assigned, and more.

<img width="1566" height="678" alt="image" src="https://github.com/user-attachments/assets/37532032-992e-4c84-a1a5-f0ac05a4b22c" />
<br>

## IAM Policy Simulator
<br>

You can use the IAM Policy Simulator to test the effects of AWS IAM policies to test your existing IAM policies to verify that they have the intended effect and capture the Policy Simulator output to use as supporting evidence in user access reviews.
<br>

Choose the ```Permissions``` tab. In the ```Permissions policies``` section, notice there is one policy attached to the user. The Attached via column shows that the ```ReadOnlyAccess``` policy is attached to ```user-1``` via the ```user1group``` IAM group.

<img width="1528" height="299" alt="image" src="https://github.com/user-attachments/assets/24d4b480-f14c-443f-a8bc-eceb1570a374" />
<br>

To run the IAM Policy Simulator, open the following link in a new web browser tab: [IAM Policy Simulator](https://policysim.aws.amazon.com/home/index.jsp#).
<br>

On the ```IAM Policy Simulator``` page, in the Users, Groups, and Roles pane, choose ```user-1```.

<img width="476" height="229" alt="image" src="https://github.com/user-attachments/assets/051c3258-f748-4950-91de-bda4aa5a86c3" />
<br>

In the Policy Simulator pane, on the ```Select service``` drop-down menu, choose ```Identity and Access Management```.

<img width="189" height="79" alt="image" src="https://github.com/user-attachments/assets/b5ed242c-bafa-4bdb-9bc0-9c06f9f73397" />
<br>
<img width="312" height="280" alt="image" src="https://github.com/user-attachments/assets/a8d87965-af9a-451d-b702-501c4d7b13d0" />
<br>

On the ```Select actions``` drop-down menu, select the following options:
* DeleteGroup
* DeleteRolePolicy

<img width="355" height="84" alt="image" src="https://github.com/user-attachments/assets/dd22980e-887f-4964-8f44-833216833f2f" />
<br>
<img width="844" height="587" alt="image" src="https://github.com/user-attachments/assets/6545f968-e975-4cea-abdf-edec0ad5d07c" />
<br>

Choose ```Run Simulation```.

<img width="1365" height="290" alt="image" src="https://github.com/user-attachments/assets/37fe6914-ba07-4a7e-b181-8cc93f861a18" />
<br>

Expected output: The Action Settings and Results section displays the effective permissions for ```user-1```, similar to this:

<img width="1363" height="293" alt="image" src="https://github.com/user-attachments/assets/7e1839bd-53da-4898-b3f9-1e26414a0175" />
<br>

Recall that the policy attached to ```user-1``` is a ```read-only policy```. Any actions that could allow changes to a service or resource are denied.


