# Google Compute Instance Templates

##### _This repository provides instructions on how to create a Google Compute Instance Template on Google Cloud Platform (GCP)._

What is a Google Compute Instance Template?

A Google Compute Instance Template is a reusable configuration for creating virtual machine instances on GCP. It defines the machine type, boot disk image, network settings, and other parameters for a new instance.

Using an instance template can save time and reduce errors when creating multiple instances with similar settings. You can modify the template to make changes to all instances that are created from it.

### Steps to Create a Google Compute Instance Template

- Go to the Google Cloud Console (https://console.cloud.google.com/).
- If you haven't already, create a project by clicking the project dropdown menu on the top navigation bar and selecting "New Project". Give it a name and click create.
- Select the project you just created from the dropdown menu.
  On the left-hand navigation menu, click on "Compute Engine" -> "Instance templates".
- Click on the "Create instance template" button.
  Give your template a name and description (optional).
- Under "Machine configuration", select the machine type you want to use.
- Under "Boot disk", select the disk image you want to use.
- Under "Firewall", select the firewall rules you want to apply.
- Under "Networking", select the network and subnet you want to use.
  Click "Create" to create your instance template.

> Different Ways to Use a Google Compute Instance Template
> Once you have created an instance template, you can use it to create instances in several ways:

## Option 1: Create an Instance from the Template in the Google Cloud Console

_1.Go to the Google Cloud Console (https://console.cloud.google.com/).
On the left-hand navigation menu, click on "Compute Engine" -> "VM instances".
2.Click on the "Create instance" button.
Under "Boot disk", select "Instance template" from the "Create from" dropdown menu.
3.Select the instance template you want to use from the "Instance template" dropdown menu.
Give your instance a name and select other settings as needed.
Click "Create" to create your instance._

## Option 2: Use the GCP API to Create Instances from the Template

_You can use the GCP API to create instances from an instance template. Here is an example command:_

```
gcloud compute instances create example-instance --source-instance-template=example-template
```

_Replace example-instance with the name you want to give your new instance, and example-template with the name of your instance template._

## Option 3: Use Terraform or Other Automation Tools to Create Instances from the Template

_You can use infrastructure-as-code tools like Terraform to automate the creation of instances from an instance template._

```resource "google_compute_instance" "example-instance" {
  name         = "example-instance"
  machine_type = "e2-micro"
  boot_disk {
    initialize_params {
      image = "debian-cloud/debian-11"
    }
  }
  network_interface {
    network = "default"
    subnetwork = "default"
  }
  source_instance_template = google_compute_instance_template.example-template.self_link
}

resource "google_compute_instance_template" "example-template" {
  name        = "example-template"
  machine_type = "e2-micro"
  boot_disk {
    initialize_params {
      image = "debian-cloud/debian-11"
    }
  }
  network
```
