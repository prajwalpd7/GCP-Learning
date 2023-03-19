## Creating a Google Compute Managed Instance Group

This assignment involves creating a Google Compute Managed Instance Group with an autoscaling configuration of minimum 1 and maximum 2 instances, using a previously created instance template.

### Prerequisites

- A Google Cloud Platform (GCP) account with billing enabled
- Basic understanding of GCP and Google Compute Engine (GCE)
- Instance template created in an earlier assignment

## Steps

1.  **Create a Google Compute Managed Instance Group:**

- Go to the Google Cloud Console and select your project.
- Navigate to the Compute Engine section.
- Select "Instance groups" from the left-hand menu.
- Click on the "Create instance group" button.
- Choose "Managed instance group" and click "Continue".
- Give the group a name and description.
- Select the region and zone where you want to create the group.
- Choose the instance template that you created in earlier Assignment, either by selecting it from the list or by entering its name.
- Click on "Create" to create the instance group.

2.  **Set the autoscaling config to Min as 1 and Max as 2:**

- After creating the instance group, click on the group name to open its details page.
- Select the "Autoscaling" tab.
- Set the minimum number of instances to 1 and the maximum number of instances to 2.
- You can also set other parameters, such as the target CPU usage or load balancing utilization, to trigger autoscaling.
- Click on "Save" to save the autoscaling configuration.

## note -

creating and managing individual VMs can be a time-consuming and error-prone task, especially when you need to handle a large number of instances. This is where Google Compute Managed Instance Groups come into play. A Managed Instance Group is a powerful feature that allows you to manage a group of VMs as a single entity, providing automated scaling, load balancing, and health checking.

> Automated Scaling: With a Managed Instance Group, you no longer need to manually create, configure, or delete VMs as traffic patterns change. Instead, you can set the minimum and maximum number of instances for the group, and the group will automatically create or remove instances as needed to maintain the desired capacity.

> Load Balancing: Managed Instance Groups also come with built-in load balancing, which distributes traffic across all instances in the group, ensuring that no single instance is overloaded. This helps you to maintain the performance and availability of your application, even during peak traffic times.

> Health Checking: Another important feature of Managed Instance Groups is health checking, which ensures that all instances in the group are healthy and operational. If an instance fails a health check, it is automatically removed from the group, and a new instance is created to replace it.
