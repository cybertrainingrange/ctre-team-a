# Network Load Balancer

<p align="center">
<img width="575" alt="Screenshot 2023-05-15 at 6 27 37 PM" src="https://github.com/cybertrainingrange/ctre-team-a/assets/119987538/8529b51c-4c91-4d0e-b2aa-bcd10e94fd52">
</p>
<p align="center">
<sup>Image by AWS</sup>
 </p>


AWS offers a wide range of cloud services that provide companies the capability to reach and service the population on a global scale and in an instant. One tool that helps accomplish this goal is a Network Load Balancer (NLB). A NLB is a service that helps handle a large number of requests targeted at a web application such as a website that hundreds of thousands are accessing simultaneously. NLB operates in the 4th layer of the OSI model which is known as the Networking layer. It supports TCP, TLS and UDP as well. When creating your load balancers you can specify what's called a target group - that's where you want the traffic to go. A listener essentially acts as a GPS and helps direct traffic received by the NLB to the selected target group.

## Configure Cloud Front - EC2 OR Load Balancer
1. In the Amazon CloudFront console, click Create Distribution
2. Click Get Started in the Web section.
3. In Origin Domain Name enter the DNS or domain name from your elastic load balancer or EC2 instance.
4. Click Create Distribution
5. When your distribution is deployed, confirm that you can access your content using your new CloudFront URL or CNAME. Copy the Domain Name into a web browser to test.


# Auto Scaling Group

<p align="center">
<img width="329" alt="Screenshot 2023-05-15 at 7 45 47 PM" src="https://github.com/cybertrainingrange/ctre-team-a/assets/119987538/ea7300e7-4412-4126-8401-2ed80828564d">
</p>
<p align="center">
<sup>Image by AWS</sup>
 </p>
 
 
An Autoscaling Group is a feature of cloud computing services that allows users to automatically adjust the number of compute resources (such as virtual machines or containers) in response to changes in demand for their applications or services. With an Autoscaling Group, users can set minimum and maximum limits on the number of compute resources, and the system will automatically add or remove resources as needed to maintain performance and availability. Autoscaling Groups can be used to handle sudden spikes in traffic, reduce costs during periods of low demand, and provide greater reliability and resilience for applications running in the cloud.

## Configure Network Load Balancer With EC2 Auto Scaling Group 
1. In EC2 Console, click Launch template
2. Configure template. In the User data, paste metadata from the instance:
```

#!/bin/bash
sudo yum install -y httpd
sudo systemctl start httpd
sudo systemctl enable httpd
sudo sh -c 'curl -s http://169.254.169.254/latest/meta-data/placement/availability-zone | perl -pe "s/^/Availability Zone: /" [REPLACED] /var/www/html/index.html'
```

3. In Autoscaling group, click Create Autoscaling Groups, and assign VPC and AZs. 
4. Choose no load balancer for now then hit next. For group size,  select 2 for desired 2 for minimum and 5 for maximum. 
5. Leave everything else at default, and click Create. 
6. In target groups, click Create. Choose instances as your target type then give your target group a name. 
7. For protocol, select TCP. For health check protocol, select HTTP. Create. 
8. In Load balancer, click Create Network Load balancer. 
9. Give your load balancer a name and leave the scheme to internet-facing and IP address type to IPV4. For Network mapping, select US East 1A and 1B. In the listeners and routing section, select the target group that we just created then hit create. 
10. In the left menu, click on the auto-scaling groups then go inside it and hit edit. Scroll down to the load balancing section, check the first check box then select our Target group then hit update. 
11. In ec2 instances and select one of the instances that were created by our Autoscaling group, copy the IP address and paste it into a browser. As you can see, this instance is running in the US East 1A Availability Zone. Check the IP address of the second instance and confirm that it's running in the US East 1B availability Zone. Now, let's go back to our Network load balancer and copy the DNS name URL and paste it into a browser window. Looks like our NLB is routing to the instance running on the US East 1B availability Zone. If one availability zone goes out, the other one activates. Check by stopping one instance. 


## 🔗 Authors: 
### Nancy Uddin
[![linkedin](https://img.shields.io/badge/linkedin-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)] (https://www.linkedin.com/in/nancy-uddin/)

### Victor Walker 
[![linkedin](https://img.shields.io/badge/linkedin-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)] (https://www.linkedin.com/in/victor-walker-iv-b2001118a/)
