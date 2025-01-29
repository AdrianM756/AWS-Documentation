## EC2 Instance

[EC2 Instance](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/concepts.html) is a virtual server in the AWS Cloud. When you start an EC2 instance, the instance type that you specify will determine the hardware available to your instance. Each instance offers a different types and balance of compute, memory, network, and storage resources depending on your needs.

## Creating an EC2 Instance

On the searc bar, type ```EC2``` and click the first one that appears.

![image](https://github.com/user-attachments/assets/060f8886-4c74-47d0-a487-b7ec99f506fe)

On the **EC2 Dashboard**, go to the Launch **instance tab**, and click on **Launch instance**.

![image](https://github.com/user-attachments/assets/0cbfb280-3182-4b29-b004-bcba6fa2b187)

Under the **Name and tags**, input your desired name for the instance (for this example, we will be using the name ```webserver1```). Scroll down on the **Application and OS Images** and select ```Amazon Linux``` as the operating system.

![image](https://github.com/user-attachments/assets/a8492852-f68b-41d4-99f1-d4ca280398c3)

Scroll down and go to the **Amazon Machine Image(AMI)** and select ```Amazon Linux 2 AMI(HVM)```.Then on the **Instance type**, select ```t2.micro```.

![image](https://github.com/user-attachments/assets/0b9cf22e-71bb-47f4-a527-b863904bb233)

On the **Key pair (login) tab**, select **Proceed without a key pair**.

![image](https://github.com/user-attachments/assets/2e7868f7-4765-4616-beb2-c13acb787a33)







