# DataCabinet

DataCabinet is an online platform to maintain your Jupyter notebooks and conda environments. It is powered by a distributed system running on AWS.

#### **Features**:
- Jupyter notebooks with support for python or R on your web browser. Other kernels can be manually installed.
- Isolated Conda environments with their own package dependencies as DataCabinet projects.
- A dedicated disk and a shared disk to easily share projects and environments.

## **Get started**
- [Register](#register)<br /> 
- [Login](#log-in)<br /> 
- [Create Project](#create-project)<br /> 
- [Install packages](#install-packages-for-environment)<br /> 
- [Export Project](#export-project)<br />
- [Import Project](#import-project)<br />
- [Code](#code)<br /> 


## **Register**

You can register your account at [datacabinet systems](http://datacabinet.systems/#/register). After registering, you will be sent an e-mail for verification after which your account would be ready to login.  <br/> 
<br /> 

<img src="Register_Final.jpg" alt="Register" style="width: 900px;"/> 


## **Log in**
Go to [datacabinet systems](http://datacabinet.systems/) to login. You can either login using your credentials or use your google account.

* Normal Login Screenshots
* Google Login Screenshots


## **Create project**

A DataCabinet project comprises of a set of user code files and one conda environment. The conda environment can have package dependencies (like tensorflow or keras), notebook extensions (nbgrader, nbpresent), language kernels for notebooks etc.

To add a project, first you need to sign-in using your credentials or google account. <br/> 
<br/> 

<img src="Project.jpg" alt="Create Project" style="width: 900px;"/> 


## **Install packages for environment**

Every project you create in DataCabinet has a corresponding Conda environment with the same name as the project.

You can install additional packages for a project using either **conda install packagename** or **pip install packagename**.

> <span style="color:red"> In the Datacabinet platform, there are some installations that interfere with functioning and should not be pip installed. A list of these are - TBD </span>

A sample installation of a package **numpy** is highlighted below:<br/> 
<br/> 

<img src="pip1.jpg" alt="Package Install" style="width: 900px;"/>


# **Jupyter Notebooks & Project Sharing**

## **Creating Notebooks**

Using Jupyter you can create lots of interesting stuff: from simple notebooks to math-heavy presentations and autograded assignments. To get started with Jupyter go to [Jupyter Notebook Basics](http://jupyter-notebook.readthedocs.io/en/latest/examples/Notebook/Notebook%20Basics.html).

You can also can install various language kernels and create notebooks in multiple languages.

To create a notebook, on the **Files** tab, click the **New** button.

## **Export Project**
Datacabinet allows you to export your project at any point. A common example would be to provision a project by installing a set of packages, writing some code in notebooks and then exporting it. Other users can import that project (using the share ID provided) and get a copy of the project exactly at the point the original user exported it.

You can share this ID with anyone, you want to share the project with.

To export a project, you need to login using your credentials or your google account. The next steps are mentioned below: <br/> 
<br/> 


<img src="export.jpg" alt="Export Project" style="width: 900px;"/>


## **Import Project**

To import a project, you need to login using your credentials or your google account. The next steps needed to import a project are highlighted below- <br/> 
<br/> 

<img src="import.jpg" alt="Export Project" style="width: 900px;"/> 




## **Code**

When you finish writing code in the created file or just want to check current progress, just go to **Cell** &gt; **Run Cells**. The result will be displayed in the new dialog.

DataCabinet provides you with the space on the NFS share (2GB) which allows you to publish your code using unix authorization mechanisms.











  
