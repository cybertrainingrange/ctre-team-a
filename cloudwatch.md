# Amazon CloudWatch
**by: Ameha Zewde Lemma and Victor Walker, IV.**

![App Screenshot](https://drive.google.com/uc?export=view&id=1wzImfY5CJoWL2liw0uZ3c-TaLAogsmyb)


If you ever wonder how that AWS infrastructure you deployed was doing, or need to learn how to leverage Aws Cloudwatch, don't worry we got you covered. Amazon Cloud Watch automatically collects and provides metrics for CPU Utilization as well. Cloud Watch is a great way to measure and track metrics. Creating alarms is a way to accomplish this because you can watch metrics and send notifications or automatically change the resource you monitor when a certain threshold is exceeded. Cloudwatch offers a wide range of solutions for your infrastructure and gives you visibility into resource utilization, Application Performance, and operational health. Overall, Cloud watch is a great way to access your AWS resources in real-time to see what is happening, and also Cloud watch is a great way to provision what resources are using too much CPU and make changes as necessary.

Amazon CloudWatch is a monitoring and management service that provides data and actionable insights for AWS, hybrid, and on-premises applications and infrastructure resources. Amazon CloudWatch collects and visualizes real-time logs, metrics, and event data in automated dashboards to streamline your infrastructure and application maintenance.

Amazon CloudWatch provides a reliable, scalable, and flexible monitoring solution that you can start within minutes. You no longer need to set up, manage, and scale your own monitoring systems and infrastructure. This tool gives you the visibility you need to spot issues before they impact the business and allow you to improve your security posture and reduce the risk profile of your environment.

Amazon CloudWatch is a monitoring service for AWS cloud resources and the applications you run on AWS. CloudWatch is used to collect and track metrics, collect and monitor log files, and set alarms.
With CloudWatch, you can:
Gain system-wide visibility into resource utilization.
Monitor application performance.
Monitor operational health.

Amazon Cloud Watch provides real-time monitoring for Aws resources such as EC2 Instances, Elastic Block storage Volumes, Elastic Load Balancer, and Relational Database Service, to name a few. 


|  ![App Screenshot](https://drive.google.com/uc?export=view&id=15dE076XRlDkw_tLJb3z6-eIr9ga1-4PL)   |
| :-------------------------------- |
|  CloudWatch provides a centralized view of an AWS environment's operational health and performance, making it easier to detect issues, troubleshoot problems, and optimize resource utilization. It can also set alarms and automate actions based on defined thresholds and metrics. CloudWatch enables you to monitor your complete stack (applications, infrastructure, network, and services) and use alarms, logs, and events data.

Some of the main features of AWS CloudWatch include: |


## CloudWatch Metrics: 
CloudWatch can collect and store metrics from various AWS services and custom applications, which can be used to create dashboards and generate alarms. CloudWatch allows you to collect, monitor, and store metrics for various AWS resources and applications. Metrics are numerical data points that represent the performance of your system, such as CPU usage, network traffic, or disk space utilization. Metrics are services that send time-ordered data points to CloudWatch. You can view these metrics in graphical form in CloudWatch dashboards and set alarms to notify you when certain thresholds or conditions are met. CloudWatch Metrics can be collected from a wide range of AWS services, including Amazon EC2, S3, Amazon RDS, Amazon DynamoDB, Lambda, and more. For example EC2 metrics are sent every 5 minutes by default (free). Detailed EC2 monitoring sends every 1 minute (Chargeable).

## CloudWatch Logs: 
CloudWatch Logs centralizes logs from systems, applications, and AWS services. It is a centralized collection of system and application logs. CloudWatch can collect, monitor, and analyze logs from AWS resources and applications, providing insights into the system's behavior. CloudWatch also allows you to collect, monitor, and analyze logs from your AWS resources and applications. Logs are text-based data that record events and activities in your system, such as errors, requests, or transactions. CloudWatch Logs allows you to store and retain these logs for long periods and provides powerful search and filter capabilities to help you quickly find and analyze the data you need. You can also set up alarms based on log events, and use CloudWatch Logs to gain insights into the performance, availability, and security of your AWS environment.

## CloudWatch Events: 
CloudWatch Events delivers a stream of system events that describe changes in AWS resources. CloudWatch Events are systems events relating changes to AWS resources and can trigger actions. CloudWatch can capture and respond to events from various sources, such as AWS services, custom applications, or external systems, and trigger automated actions based on these events.CloudWatch Events lets you capture and respond to events from various sources, such as AWS services, custom applications, or external systems. Events indicate a change or activity in your system, such as creating a new EC2 instance or a failed deployment. CloudWatch Events can be used to trigger automated actions based on these events, such as running a Lambda function, sending a notification, or creating a backup. It can automate your workflows and reduce manual intervention in your system.

## CloudWatch Alarms: 
CloudWatch Alarms allows you to create alarms that notify you when certain thresholds or conditions are met, such as CPU usage, network traffic, or error rates. CloudWatch Alarms monitor metrics and initiate actions. CloudWatch alarms monitor metrics and can be configured to initiate actions automatically. Alarms can be based on metrics, logs, or events, and can be used to monitor the health and performance of your system. For example, you can create an alarm that triggers when the CPU usage of an EC2 instance exceeds a certain threshold or when the number of errors in your application logs exceeds a specific limit. CloudWatch Alarms can be integrated with other AWS services, such as Amazon SNS or AWS Lambda, to automate actions and alerts.
There are two types of alarms:
| - Metric Alarm: Performs one or more actions based on a single metric
- Composite Alarm: Uses a rule expression and takes into account multiple alarms.
Metric Alarm states:
- OK - Metric is within a threshold
- ALARM - Metric is outside a threshold
- INSUFFICIENT_DATA - not enough data |


In summary, AWS CloudWatch is essential for monitoring, troubleshooting, and optimizing AWS resources and applications. It can help you identify issues before they impact your users and take proactive measures to ensure the availability, reliability, and performance of your AWS environment. CloudWatch is a powerful tool that provides comprehensive monitoring and observability capabilities for your AWS environment. It can help you identify and diagnose issues quickly, optimize your resource utilization, and ensure the availability and reliability of your system. 


## 🛠 Technical Documentation
[AWS CloudWatch Summary](https://docs.google.com/document/d/1GDviH7ZmXk3-k1BgSpSs8wmL0UZIa83SvoWhLk0ZOWE/edit?usp=share_link)

[AWS CloudWatch Technical Documentation](https://docs.google.com/document/d/1fDODmdVfspMcIQxkZpRRMyq2a0zFhFwirc3aPRr1kMA/edit?usp=share_link)


## 🔗 Authors: 👐

### Ameha Zewde Lemma 👨
[![linkedin](https://img.shields.io/badge/linkedin-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/ameha-lemma/)
- [@Ameha Zewde Lemma](https://github.com/orgs/cybertrainingrange/people/ameha01)

### Victor Walker👨
[![linkedin](https://img.shields.io/badge/linkedin-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/victor-walker-iv-b2001118a/)
- [@Victor Walker](https://github.com/orgs/cybertrainingrange/people/vick627)

