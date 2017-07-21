# DataCabinet

Getting started guide

# **Introduction**

DataCabinet is a cloud-based IDE for Machine Learning.

DataCabinet allows you to start building your Machine Learning projects in just a few clicks and without worrying about machine provisioning or tool installation. We offer:

- Jupyter notebooks with support for python or R on your web browser
- Isolated Conda environments with their own package dependencies
- Load balanced and auto-scaled backend running on AWS

# **Get started**

## **Register**

To register in DataCabinet:
1. Go to [systems](http://datacabinet.systems) and complete the form.     
![](https://github.com/datacabinet/datacabinet-info/blob/66dec31555b7e4d8f0bdca3ad3ccdcebd598f3d7/images/register_step_1.png?raw=true)
1. After completion of the registration form, a confirmation email is sent to your mail address.
![](https://github.com/datacabinet/datacabinet-info/blob/66dec31555b7e4d8f0bdca3ad3ccdcebd598f3d7/images/register_step_2.png?raw=true)
1. Follow the link in the email to verify your email address.
![](https://github.com/datacabinet/datacabinet-info/blob/66dec31555b7e4d8f0bdca3ad3ccdcebd598f3d7/images/register_step_3.png?raw=true)
1. Log into DataCabinet using your credentials.

## **Log in**
When you log in DataCabinet and have an open session on other device, you can forcefully disconnect from that hard drive be selecting the Force Detach Hard Drive check box.  
![](https://github.com/datacabinet/datacabinet-info/blob/9e5219d3eb374d4699d64889e173f7cb61ce6548/assets/base/log_in_disconnect_hard_drive_from_login_window.jpg?raw=true)

If you do not remember having an open session on other device, this button will remind you: ![](https://github.com/datacabinet/datacabinet-info/blob/9e5219d3eb374d4699d64889e173f7cb61ce6548/assets/base/log_in_disconnect_hard_drive_needed_after_login.jpg?raw=true) - click it to disconnect. When this button is green (![](https://github.com/datacabinet/datacabinet-info/blob/9e5219d3eb374d4699d64889e173f7cb61ce6548/assets/base/log_in_no_disconnect_hard_drive.jpg?raw=true)) - no other hard drives are connected.


## **Create project**

In DataCabinet, python projects are used to store all your code, python/conda-related binaries, and package dependencies.

To add project:

1. Log in using your credentials.  
1. On the main page of DataCabinet, click **Project** , and then click **Add New Project**.  
![](https://github.com/datacabinet/datacabinet-info/blob/66dec31555b7e4d8f0bdca3ad3ccdcebd598f3d7/images/create_project_step_2.png?raw=true)
1. In the **Enter project details** dialog, expand the drop-down list, and then select the needed project type.  
![](https://github.com/datacabinet/datacabinet-info/blob/66dec31555b7e4d8f0bdca3ad3ccdcebd598f3d7/images/create_project_step_3.png?raw=true)
1. In the **Enter project details** dialog, do the following:
    1. Select the needed Python version.
    1. Enter name of project.
    1. Enter password to project.  
    ![](https://github.com/datacabinet/datacabinet-info/blob/66dec31555b7e4d8f0bdca3ad3ccdcebd598f3d7/images/create_project_step_4.png?raw=true)
1. Click **OK**.

The project will be created in approximately 30 minutes in the directory /mnt/ebs/&lt;your email&gt;.

## **Install packages for environment**

Every project you create in DataCabinet has a corresponding a Conda environment with the same name as the project.

You can install additional packages for a project using either conda install &lt;pkg&gt; or pip install &lt;pkg&gt; and they are installed in the /mnt/ebs/[name/email] [/CodingTheMatrix/.conda](http://gmail.com/CodingTheMatrix/.conda)directory.

To install package go to **New &gt; Terminal** , and then execute the following command as in the example using the name of needed package.  
![](https://github.com/datacabinet/datacabinet-info/blob/66dec31555b7e4d8f0bdca3ad3ccdcebd598f3d7/images/install_packages.png?raw=true)

## **Create notebook**

To create notebook, on the **Files** tab, click the **New** button.

Using Jupyter you can create lots of interesting stuff: from simple notebooks to math-heavy presentations and autograded assignments. To get started with Jupyter go to [Jupyter Notebook Basics](http://jupyter-notebook.readthedocs.io/en/latest/examples/Notebook/Notebook%20Basics.html).

You can also can install various language kernels and create notebooks in multiple languages.

## Code!

When you finish writing code in the created file or just want to check current progress, just go to **Cell** &gt; **Run Cells**. The result will be displayed in the new dialog.

DataCabinet provides you with the space on the NFS share (2GB) and allows you to synchronize your Google Drive and Dropbox storages with it.

You have two directories in DataCabinet:
* /mnt/nfs/&lt;your email&gt; directory] - your personal directory where you configure access rights to the projects and files using Unix file permissions.
* /mnt/ebs/&lt;your email&gt; directory] - general directory where all users have access to projects and files.
