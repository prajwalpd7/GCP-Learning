## Google Cloud Storage Bucket Assignment

Instructions for creating a Google Cloud Storage Bucket with versioning enabled and uniform access control.

### Prerequisites

- A Google Cloud Platform account
- Basic knowledge of the Google Cloud Console

### steps -

1.  Log in to your Google Cloud Console.
2.  Navigate to the Cloud Storage section.
3.  Click on the "Create bucket" button.
4.  Choose a unique name for your bucket.
5.  Select a region where you want your bucket to be stored. For this task, select a single region.
6.  Choose the default storage class.
7.  Click on "Create".

### Creating a Folder and Uploading Files

1.  Click on your newly created bucket to open it.
2.  Click on the "Create folder" button and give it a name.
3.  Click on the folder you just created to open it.
4.  Click on the "Upload files" button.
5.  Select the files you want to upload (i.e any text files).
6.  Click on "Open" to upload the selected files to your folder.

### Enabling Object Versioning

1.  In the Google Cloud console, go to the Cloud Storage **Buckets** page.  
    [Go to Buckets](https://console.cloud.google.com/storage/browser)
2.  In the list of buckets, click on the name of the bucket on which you want to enable or disable Object Versioning.
3.  Select the **Protection** tab near the top of the page.
    The current status of Object versioning is found in the **Object versioning** section
4.  In the **Object versioning** section, click the current status to make changes to it.
    The **Object versioning** dialog box appears.
    a. If you're enabling Object Versioning and you want to minimize storage costs, select the **Add recommended lifecycle rules to manage version costs** checkbox.
5.  Click **Confirm**.

\_Enabling object versioning means that when a new version of an object (i.e file) is uploaded to your bucket, the old version is kept as well. This allows you to keep a history of changes made to your files.

### Setting Access Control to Uniform

_Setting access control to uniform means that all objects in the bucket have the same access control settings. This can simplify access control management, as you only need to set the access control once for the entire bucket._

### Acknowledgments

- [Google Cloud Storage Documentation](https://cloud.google.com/storage/docs) for providing detailed instructions and examples.
