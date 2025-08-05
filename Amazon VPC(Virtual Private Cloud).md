## Amazon VPC

[Amazon VPC(Virtual Private Cloud)](https://docs.aws.amazon.com/vpc/latest/userguide/what-is-amazon-vpc.html) is a service from AWS that lets you create a **logically isolated network** within the cloud. It allows us to isolate resources from other resources and gives full control of networking in the cloud.
<br>

**NOTE:** VPC is specific to single region. **It cannot** reach mulltiple regions. Therefore, you cannot have the same VPC across Regions. this is not allowed. For more in-depth regarding to this, you can visit this [link](https://repost.aws/articles/ARgs1iWM-ASlGSktYepaY68Q/networking-101-part-2).
<br>


Go to the search bar and type  ```vpc```. click the first result that appears.
<br>
<img width="941" height="348" alt="image" src="https://github.com/user-attachments/assets/6bf7b7c0-46a3-4eea-b264-071f2e61c305" />
<br>

Click on ```VPCs```.
<br>
<img width="617" height="225" alt="image" src="https://github.com/user-attachments/assets/c191af42-049a-4d7e-b6f6-97743ff0a4b2" />
<br>

**NOTE:** By Default, AWS is going to create a default VPC on every region with same exact configuration. This includes IPv4 CIDR block of ```172.31.0.0./16```.
<br>

Right now where in the US East ( N. Virginia) region or ```us-east-1``` for short. 
<br>
<img width="927" height="143" alt="image" src="https://github.com/user-attachments/assets/8774f1e9-3303-4231-b780-93c62d69fcaf" />
<br>

If we go to another region like uS East (Ihio) or ```us-east-2```, we can see another default VPC.
<br>
<img width="1061" height="146" alt="image" src="https://github.com/user-attachments/assets/5c26c3b8-75bc-4187-b301-74cc9e128955" />
<br>

Now let's go back to our VPC in ```us-east-1``` and click on the ```Subnets```. You will see that there are a total of 6 subnets that are associated with our default VPC.
<br>
<img width="1675" height="297" alt="image" src="https://github.com/user-attachments/assets/75d4ef62-cbcd-45b8-b2ad-4941b3e59556" />
<br>

*Question:* Why does it have 6 subnets that are associated on our default VPC and why does it matters?
<br>
<br>

*Answer:* These 6 subnets where created on our default vpc, one for each [Availability Zone (AZ)](https://docs.aws.amazon.com/global-infrastructure/latest/regions/aws-availability-zones.html) in the region. It's going to creata  default subnet for each availability zones.
<br>
<img width="440" height="218" alt="image" src="https://github.com/user-attachments/assets/ddf09247-e654-400f-acae-03e6eeb32820" />
<br>

By going back to our VPC ang navigating to the ```Resource Map```, We can see a more visualize graph of it.
<br>
<img width="946" height="692" alt="image" src="https://github.com/user-attachments/assets/09ee5809-861e-426e-8c1a-5dbc4ba01d01" />
<br>

Because we have internet gateway assigned on this VPC, we automatically have internet access. If we select one of the subnets, We can see that in the ```Auto-assign public IPv4 address``` that is set to ```Yes```.
<br>
<img width="1476" height="460" alt="image" src="https://github.com/user-attachments/assets/cb9c132e-c9f5-4c95-906f-0862829ce57a" />
<br>
This means, that if we deploy an EC2 instance, it will automatically recieve an Public IP Address. 

