# DataCabinet

Getting started guide

# **Introduction**

DataCabinet is a online platform to maintain your Jupyter notebooks and conda environments.

DataCabinet offers:
- Jupyter notebooks with support for python or R on your web browser. Other kernels can be manually installed.
- Isolated Conda environments with their own package dependencies as DataCabinet projects
- A dedicated disk and a shared disk to easily share projects and environments.

It is powered by a distributed system running on AWS.

# **Get started**

## **Get Access Code**
<span style="color:blue">*DataCabinet product is in beta. Users can register but you will need an access code to launch the notebooks. Please use Sign Up link on the
landing page and we will send you an access code: [landing page](http://datacabinet.info)*</span>

## **Register**

To register in DataCabinet:
1. Go to [datacabinet systems](http://datacabinet.systems/#/register) and complete the form.     
1. After completion of the registration form, a confirmation email is sent to your mail address.
1. Follow the link in the email to verify your email address.
1. After you receive the email that your datacabinet account is ready, Log into DataCabinet using your credentials.

## **Log in**
Go to [datacabinet systems](http://datacabinet.systems/) to login.

- After login, your hard drive is not available if there is another session still running. You can force the hard drive to connect to your current session
This button will remind you if you have another session going on: ![](https://github.com/datacabinet/datacabinet-info/blob/9e5219d3eb374d4699d64889e173f7cb61ce6548/assets/base/log_in_disconnect_hard_drive_needed_after_login.jpg?raw=true). It will disconnect the other session if you click it. When this button is green (![](https://github.com/datacabinet/datacabinet-info/blob/9e5219d3eb374d4699d64889e173f7cb61ce6548/assets/base/log_in_no_disconnect_hard_drive.jpg?raw=true)) - the hard drive is correctly attached to the current session.

- You will need to enter an access code to be able to run Jupyter notebooks:
![](https://github.com/datacabinet/datacabinet-info/blob/6e9deeb35c62944e8f7354ef3e1179bfeee7fa84/images/access_code1.png?raw=true)
![](https://github.com/datacabinet/datacabinet-info/blob/6e9deeb35c62944e8f7354ef3e1179bfeee7fa84/images/access_code2.png?raw=true)

## **Create project**

A DataCabinet project comprises of a set of user code files and one conda environment. The conda environment can have package dependencies(like tensorflow or keras), notebook extensions(nbgrader, nbpresent), language kernels for notebooks etc.

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

The project will be created in approximately 5 minutes in the directory /mnt/ebs/&lt;your email&gt;/&lt;Project Name&gt;.

## **Install packages for environment**

Every project you create in DataCabinet has a corresponding a Conda environment with the same name as the project.

You can install additional packages for a project using either conda install &lt;pkg&gt; or pip install &lt;pkg&gt; and they are installed in the &lt;your email&gt;/&lt;Project Name&gt;/.conda directory.

To install package go to **New &gt; Terminal** , and then execute the following command as in the example using the name of needed package. 
![](https://github.com/datacabinet/datacabinet-info/blob/3f78634c07e4f6423d31fcccc8775e61f8aae4c0/images/install_packages.png?raw=true)

## **Create notebook**

To create notebook, on the **Files** tab, click the **New** button.

Using Jupyter you can create lots of interesting stuff: from simple notebooks to math-heavy presentations and autograded assignments. To get started with Jupyter go to [Jupyter Notebook Basics](http://jupyter-notebook.readthedocs.io/en/latest/examples/Notebook/Notebook%20Basics.html).

You can also can install various language kernels and create notebooks in multiple languages.

## Code!

When you finish writing code in the created file or just want to check current progress, just go to **Cell** &gt; **Run Cells**. The result will be displayed in the new dialog.

DataCabinet provides you with the space on the NFS share (2GB) which allows you to publish your code using unix authorization mechanisms.

You have two directories in DataCabinet:
* /mnt/ebs/&lt;your email&gt; directory] - your personal directory which is not seen by others.
* /mnt/nfs/&lt;your email&gt; directory] - general directory where all users have access to projects and files. You can configure access rights to the projects and files using Unix file permissions.


## NBGrader

NBGrader (http://nbgrader.readthedocs.io/en/stable/) works in a hassle free way with DataCabinet. Using NBGrader and DataCabinet, it is easy to distribute complex assignments 
with multiple dependencies to a large community of students.

**<span style="color:red">[Marketing/Landing Page:](http://datacabinet.info) </span>**

