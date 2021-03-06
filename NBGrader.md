# DataCabinet

DataCabinet is a online platform to maintain your Jupyter notebooks and conda environments.

DataCabinet offers:
- Jupyter notebooks with support for python or R on your web browser. Other kernels can be manually installed.
- Isolated Conda environments with their own package dependencies as DataCabinet projects
- A dedicated disk and a shared disk to easily share projects and environments.

It is powered by a distributed system running on AWS.

## **Get started**
[Get Access Code](#get-access-code)<br /> 
[Register](#register)<br /> 
[Login](#log-in)<br /> 
[Create Project](#create-project)<br /> 
[Export Project](#export-project)<br />
[Import Project](#import-project)<br />
[Install packages](#install-packages-for-environment)<br /> 
[Code](#code)<br /> 
[NBGrader](#nbgrader)<br /> 
[NBPresent](#nbpresent)<br /> 
[Git and Ssh](#gitssh)<br /> 

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

## **Export Project**
Datacabinet allows you to export your project at any point. A common example would be to provision a project by installing a set of packages, writing some code in notebooks and then exporting it. Some other user can then import that project (using the share ID provided) and get a copy of the project exactly at the point the original user exported it.

To export a project:
1. Log in using your credentials.
1. On the main page of DataCabinet, select the project, you want to export by clicking on the **Play** button on the project tile.
1. Click 'reload' on the browser. You will see two extra buttons on the project tile now.
1. Click on the middle **Share** button.
1. On the window that appears, click the **Generate** button.
1. Copy the 24 character ID that appears. It might take a while for the ID to appear, depending on how big your project is. 

You can share this ID with anyone, you want to share the project with.


## **Import Project**

To import a project:
1. Log in using your credentials.
1. On the main page of DataCabinet, click **Project** , and then click **Import Project**.  
1. In the **Import project ** dialog, do the following:
    1. Enter the project share ID
    1. Enter name of project.
    1. Enter password to project.  
1. Click **Import Project**.

On a reload, you should see the project tile for the new imported project. It will take a while for the project to get provisioned.


## **Code**

When you finish writing code in the created file or just want to check current progress, just go to **Cell** &gt; **Run Cells**. The result will be displayed in the new dialog.

DataCabinet provides you with the space on the NFS share (2GB) which allows you to publish your code using unix authorization mechanisms.

You have two directories in DataCabinet:
* /mnt/ebs/&lt;your email&gt; directory] - your personal directory which is not seen by others.
* /mnt/nfs/&lt;your email&gt; directory] - general directory where all users have access to projects and files. You can configure access rights to the projects and files using Unix file permissions.


## **NBGrader**
DataCabinet provides you the backend to create and distribute programming assignments using nbgrader. You can create a populated assignment with both questions and answers and then nbgrader turns it into unpopulated version which contains only questions. Then you can share the assignments with students, auto grade and/or form grade assignment, and then distribute grades. Please find more documentation about nbgrader here: http://nbgrader.readthedocs.io/en/stable/index.html 

**Prerequisite:** Install and configure nbgrader with DataCabinet:

1. Open the needed project.

2. Go to **New** > **Terminal**, and then install nbgrader:

       pip install nbgrader
       jupyter nbextension install --user --py nbgrader --overwrite
       jupyter nbextension enable --user --py nbgrader
       jupyter serverextension enable --user --py nbgrader

3. You might need to restart notebook or log out/log in again to see the changes.

4. On terminal, Run the following command to create an empty configuration file:

        nbgrader --generate-config

5. Make a directory in the nfs drive and give everyone permission to it: 

        mkdir /mnt/nfs/<your email>/share 
        chmod 777 /mnt/nfs/<your email>/share

6. Open the nbgrader_config.py file that is generated through the jupyter console and put:

        c = get_config()
        c.NbGrader.course_id = "<course id>"
        c.TransferApp.exchange_directory = "/mnt/nfs/<your email>/share/<coursename>"

**Create assignment:**

1. Open the needed project and notebook.

2. Go to View > Cell Toolbar > Create Assignment.

3. Add cells with content:

    1. Multiple cells with questions and tasks, each cell will have ID, points.

    2. Solution in a solution block and student is expected to fill it up 

    3. Assessment for you to grade answers

4. Save using File > Save and Checkpoint

5. Assign to students – in the New > Terminal execute "nbgrader assign chapter0". It create a notebook with assignment for students.

Note: If you attempt assigning to students, and new file is not created, use dash force command. This command removes the existing file and creates new one for new version.

6. To release assignment, in Terminal, execute command "nbgrader release --force chapter0 ".

You students need to know how to access release shared directory.

Useful commands in nbgrader (See more info on nbgrader docs):

* Create assignment by putting the assignment notebooks in proper directory structure

* Add assignment to database – "nbgrader assignment add chapter0"

* Add a student to database – "nbgrader db student add [name]"

You can also list all needed students – "nbgrader db student list [name]"

* nbgrader assign chapter0 

* nbgrader release chapter0

**For student users**

To access assignments, student needs to install nbgrader extention. Follow the same instructions as the instructors. Only difference is that the course id and transfer directory needs to be that of the instructor:

    c = get_config()
    c.NbGrader.course_id = "<course id>"
    c.TransferApp.exchange_directory = "/mnt/nfs/<instructor email>/share/<coursename>"

To get the assignment, in Terminal, do "nbgrader fetch chapter0".

When you finish assignment, in Terminal, do "nbgrader validate chapter0".

## **NBPresent** 

Using DataCabinet, you can create presentations in the Jupyter notebook.

Jupyter notebook allows you to mix your presentations with runnable code, mathematical notation and latex symbols using MathJax.

**Prerequisite:** install the nbpresent extension. In the needed project, go to **New** > **Terminal**, and then execute command:

        pip install nbpresent
        jupyter nbextension install nbpresent --user --py --overwrite
        jupyter nbextension enable nbpresent --user --py
        jupyter serverextension enable nbpresent --user --py

Then go to the needed notebook. In the tool menu you have new buttons

![](https://github.com/datacabinet/datacabinet-info/blob/6b85ac0144e01b925be824afa49b7be66d763106/images/nbpresent_edit_play.png?raw=true) that allow creating and showing the presentation.

1. Open the needed project and notebook.

2. Go to View > Cell toolbar > Slideshow.

3. In the Slide type drop-down list, select Slide.

4. Go to Cell > Cell type, and select the needed option (Code, Markdown, and …) and enter content for your presentation.

Add as many slides as you need, using … (… button).

5. On the top menu, click the Edit presentation button. 
![](https://github.com/datacabinet/datacabinet-info/blob/6b85ac0144e01b925be824afa49b7be66d763106/images//nbpresent_edit.png?raw=true)

6. On the right panel, click Slides/Present.
![](https://github.com/datacabinet/datacabinet-info/blob/6b85ac0144e01b925be824afa49b7be66d763106/images/create_slide_view.png?raw=true)

7. Remove any slides already present by clicking the -Slide a number of times.
![](https://github.com/datacabinet/datacabinet-info/blob/6b85ac0144e01b925be824afa49b7be66d763106/images/delete_slides.png?raw=true)

8. Choose either Basic or RISE/reveal slide format. After choosing the format, press escape or press the notebook button to get back to the notebook.
![](https://github.com/datacabinet/datacabinet-info/blob/6b85ac0144e01b925be824afa49b7be66d763106/images/create_slides.png?raw=true)

9. Now you can use the present button to present. 

10. Tip: To see the source of the slide during the presentation, double-click a slide. To go back, press Ctrl + Enter.

**<span style="color:red">[Marketing/Landing Page:](http://datacabinet.info) </span>**


## **GitSsh**
The default key resides in the directory /mnt/ebs/\<email\>/.ssh directory.
If you put the public key on your git provider, you will be able to access git and ssh.

## **Common Problems**
1. My new projects do not take password
It is possible your conda cache is corrupted. `conda clean --index-cache`

