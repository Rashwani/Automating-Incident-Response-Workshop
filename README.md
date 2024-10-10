
# Automating Incident Response with AWS

This project demonstrates how to automate incident response in AWS using a combination of services, including **AWS Lambda**, **Amazon GuardDuty**, **AWS Step Functions**, and **Amazon SNS**. By automating these processes, security teams can quickly detect and respond to potential threats, improving overall security and reducing manual intervention.

## Project Overview

In this project, I developed an automated incident response solution that integrates GuardDuty findings with Lambda functions to automatically respond to detected security threats. This solution helps security teams respond to incidents faster by automating repetitive actions like isolating compromised instances, notifying teams, or disabling access keys.

### Key AWS Services Used

- **Amazon GuardDuty**: Provides continuous monitoring of your AWS environment for malicious activity or unauthorized behavior.
- **AWS Lambda**: Executes the automated response functions based on GuardDuty findings.
- **Amazon SNS**: Sends notifications to relevant stakeholders about detected threats and responses taken.
- **AWS Step Functions**: Orchestrates the incident response workflow, ensuring tasks are completed in the correct order.

### Architecture

The architecture includes the following components:

1. **GuardDuty**: Detects potential threats such as unauthorized access attempts or compromised instances.
2. **Lambda Functions**: Triggered by GuardDuty findings to execute specific response actions like isolating instances or disabling compromised keys.
3. **Step Functions**: Manages the sequence of actions to ensure that each step in the incident response process is executed properly.
4. **SNS**: Notifies administrators or security teams when incidents are detected and actions are taken.

### Incident Response Workflow

1. **Detection**: GuardDuty detects suspicious activity and generates findings.
2. **Trigger**: The finding triggers a Lambda function through an Amazon CloudWatch event.
3. **Response**: Lambda performs predefined actions such as quarantining the instance, terminating connections, or revoking permissions.
4. **Orchestration**: AWS Step Functions ensures the response is executed in a well-defined order.
5. **Notification**: SNS sends alerts to the security team, ensuring they are informed of the actions taken.

### Benefits of Automating Incident Response

- **Faster Response**: Automated workflows reduce the time to detect and respond to security threats.
- **Reduced Human Error**: Automation ensures consistent execution of response actions without manual intervention.
- **Scalability**: Automatically handle incidents across multiple AWS accounts or regions.
- **Proactive Security**: Continuously monitor and mitigate threats before they escalate.

## Setup and Deployment

To replicate this project, follow these steps:

1. **Enable Amazon GuardDuty**: Ensure GuardDuty is enabled in your AWS environment for continuous monitoring.
2. **Create Lambda Functions**: Define and deploy Lambda functions to handle specific security incidents (e.g., isolating EC2 instances).
3. **Set Up Step Functions**: Design a Step Functions workflow to orchestrate the response process.
4. **Configure SNS**: Set up an SNS topic to send notifications to your team when an incident occurs.
5. **Deploy the Solution**: Integrate GuardDuty findings with Lambda, Step Functions, and SNS for a fully automated incident response system.

## Skills and Learnings

Through this project, I gained experience in:

- Automating incident detection and response using Amazon GuardDuty and AWS Lambda.
- Building complex workflows using AWS Step Functions.
- Implementing event-driven architectures for security automation.
- Leveraging SNS for real-time notifications and alerts.

## View Project Details

You can view the project details [here](https://awsportfolio.sila.studio/project/automating-incident-response-workshop/).

## Acknowledgments

This project was completed as part of the **Digital Cloud Training** bootcamp. 


