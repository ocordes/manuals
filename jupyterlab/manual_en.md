

# Jupyterlab@AIfA - Manual

This document is the starting manual using the JupyterLab-System of the Argelander Institute for Astronomie. 

Author: Oliver Cordes - 2022-15-09

------

**Table of contents**

[TOC]


------

<div style="page-break-after: always"></div>

## 0. Prerequisites

Before you start with this manual please be sure that you're using either the *Mozilla Firefox* or *Google Chrome/Chromium* browser. We had a lot of problems with *Microsoft Edge* and *Apple Safari* browsers.

Also there is no need to install any special software on you devices, Laptop, Tables, Smart phones. You only need an internet connection a working browser and a keyboard and mouse for editing files. A big screen for your work is in any case a good solution.

------

## 1. Login into jupyterlab

The python environment is running on a server in the Argelander Institute for Astronomie. Type in the following address into any web browser:[https://jupyterhub-students.astro.uni-bonn.de]()

You will see the following login page:

![login](login.png)

For logging in press the button *Sign in with Shibboleth*. You will redirected to the university shibboleth login page:

![shibboleth](shibboleth.png)

For login please use you University-ID without the *@uni-bonn.de*. After you typed in your password, you will be redirected back to the jupyterhub page, in which you can choose your working environment (also called working profile):

![profiles](profiles.png)

On this page you can choose any existing profile which fits to the lecture or workshop or software enviroment. Your personal data will be available in the same structure in each of the profiles. The only difference may be the software environment and maybe some persistent data.

After choosing a profile you may see a page similar (only for a couple of seconds) to this:

![startup](startup.png)

If everything is going well, you will see this page only for a couple of seconds until you see the startup of the jupyterlab-enviromnent. If there is a problem during the startup please look at the FAQ at the end of this document.

After the successful start of the environment you will see this standard desktop screen:

![homescreen](homescreen.png)



The main desktop is organized like a typical gui (graphical user interface), you have a menu starting on the top left of the window, a left panel which is a file browser and a tabbed part which is the main working area. You will start always with one tab open which is the so called *Launcher*. You can add a new tab while clicking on the *plus sign +*  below the main menu.  Each new tab starts with the *Laucher*. In the top right corner you will find the logout button labled with *Log Out*. 

### 1.1 The file browser

The file browser is like the typical file browser you already know from different OSes. It shows the actual working directory and then all directories and files inside this working directory. You can switch to sub directories by clicking on some directory in the list. To move to upper directories please click on the specific directory in the working directory label. The file browser has some quick functions in a context menu which you can open by using the right hand mouse button, e.g. creating a new sub directory or renaming a file:

<img src="newdirectory.png" alt="newdirectory" style="zoom:67%;" /> 

All other functions in the context menus are most self explaining. If you double-click on a file the corresponding program will be opened in a new tab, e.g. if you double-click on a notebook, the notebook editor will be opened.

### 1.2 The Launcher

This tab is visible every time a new tab is opened. It has the main start buttons for installed tasks and programs, e.g. an editor for Python notebooks, a text editor, a linux terminal etc. 

### 1.3 Create a new python notebook

This button opens a new python notebook, normally with the filename *Untitled.ipynb* in the current working directory. Please rename the notebook directly after creation. Follow Sect. 2  for an example.

### 1.3 The Terminal

With this button a new linux terminal will be opened in a new tab:

![terminal](terminal.png)

In this terminal you can use all linux commands which are normally installed on a linux system. Please note, that only programs are working which don't use any graphical environment e.g. X11. There is no possibiliy to start any of these programs or to establish a display forwarding tunnel even if you have an X11 server started! 

### 1.4 The Contextual Help

This button starts a backgroud help system which will be described in Sect.  2.4.

### 1.5 The Upload button

Using this button opens an uploading dialog of your web browser. All choosen files will be uploaded into the current working directory of the file browser.

### 1.6 The text file editor

This button opens a new text file which is called *Untitled.txt* in the current working directory of the file browser. It can be used to create e.g. *python scripts*. Please rename the file directly after creation unsing the context menu (right mouse click) on the tab name.

------

## 2. Python notebook editor

In this setion we will show how the notebook editor is working with an example. We will create a notebook with some code and documentation.

### 2.1 Example creation of a python notebook

To create a new python notebook, use the Laucher tab (if no tab is open, use the *plus* sign in the main menu) and click on the button labled with  *Python 3* in the Notebook section. The tab will now show an empty notebook. 

![newnotebook](newnotebook.png)

The new notebook will be named something similar to *Untitled.ipynb* and will be stored in the current directory of the file browser. The first step will be to rename the notebook. For this task do a right mouse click on the tab. This will open a context menu:

<img src="renamenotebook.png" alt="renamenotebook" style="zoom: 67%;" /> 

Choose *Rename Notebook* and enter a new name for the notebook:

<img src="renamenotebook2.png" alt="renamenotebook2" style="zoom:67%;" />



Please keep in mind, that a new notebook will always be created in the current directoy of the file browser. If you want to have it in another directory please change the current directory in the file browser (see Sec. 1.1) before you create the notebook or if already created use the right mouse click for opening the context menu. You can use first *Cut* the file then *Paste* the file in the correct directory. 

### 2.2 Open an existing notebook

The simplest way is to double click on any notebook file in any directory. This will open the notebook in a new tab!

### 2.3 Writing a notebook 

After we have created an empty notebook we can write some content into the notebook.  The complete notebook is arranged by so called cells which are stacked on top of each other. The cells can have different types. The important types are *code cells* and *markdown cells*. In *code cells* you can write your program code which can be executed by an interpreter running in the background which is called *kernel*. In this example the only kernel available is a *Python* kernel. In other confiurations there are also *bash*, *Julia*, *C++* kernels available. 'Markdown cells' are typically used to write static content e.g. code documentation, exercise descriptions, images etc. 

In this example we write some python code into the first cell:

![editnotebook](editnotebook.png)

The first cell has now the Python equivalent of the typical *Hello world!*-program. After a cell was edited you can execute the content by pressing *Shift-Enter*. The result of the execution is written below the previous cell:

![runprogram](runprogram.png)

 After any execution the notebook editor will create a new empty cell and the type of this cell will be *code*. Now we want to change the type of the cell into a *mark down documentation* cell. Therefor click on the code menu of editor:

![markdown](markdown.png)

Choose *Markdown* to change the type of the cell:

![celltype](celltype.png)

Now you the layout of the cell slightly changes and you can type some content. One interesting feature of such a mark down cell is that you can use LaTeX commands e.g. equations which are displayed similar to any LaTeX documents:

![markdown1](markdown1.png) 

If you execute the cell with *Shift-Enter*, you will see the Text of the cell now rendered:

![markdown2](markdown2.png)

LaTeX commands are perfectly interpreted. 

To update existing cells in the notebook, you simply double click with your mouse double click on a cell and you are back in the edit mode. You can also change the type of the cell in the case that you started with a code cell and wanted to write some documentation. 

In any case after you've written content to the notebook you should save the complete notebook with the typical Save-Command *cmd-S* (MacOS), *Ctrl-S* (Linux, Windows?). You can also use the main menu which has all the necessary entries of a standard editor you probably know. 

### 2.4 The Run cell menu

In the editor menu there is a special menu called *Run*. With this men you can run one or many cells of your notebook. This is sometimes necessary if you create many code cells.

<img src="runmenu.png" alt="runmenu" style="zoom:67%;" />

### 2.3 The python kernel menu

Sometimes during tests of code cells you will face some problems, e.g. infinite loops. In this case the *Kernel* menu is important. Here you can find some commands to interrupt or restart the running kernel. 


<img src="kernelmenu.png" alt="kernelmenu" style="zoom:67%;" />


### 2.4 Contextual help for python notebooks

A pretty nice feature of the jupyterlab environment is the *contextual help function*. To activate this feature you need to click once in a session on the *Contextual Help* button in the Laucher tab. This opens an empty new tab. 

![](contexthelp.png)

Now go back to the notebook editor. In the first code cell we have the python command *print*. Use the left mouse click to activate the cell and click a second time on the *print* command. Then you can also use *cmd-I* (MacOS) or *Ctrl-I* (Linux/Windows) to activate the help function. The contextual help page should show the help page for the print command. If you enter a new command the help page will change if a valid command is detected.

![contexthelp2](contexthelp2.png)

------

## 3. Data transfer 

The jupyterlab environment is a closed system which is available from outside only though a web browser. There is absolutely no way to transfer data *in* and *out* of the environment if no web session is running. 

If a web session is running there are two possibilities to copy data *in* and *out*:

1. In the file browser you can use the context menu after clicking the right mouse button which provides you a *Download* entry. With this function you can download any files which is shown in the file browser. For uploading files you can use the *Upload* button (see Sect. 1.5). All uploaded files will be stored in the current working directory of the file browser.
2. The other possibility is to use any of the programs in a terminal tab. In the terminal there is a Ubuntu 18.04 Linux OS running which provides some of the common programs for data exchange, *scp*, *wget*, *git*, etc. 

------

## 4. Ending a session

The best way is to logout in the case you stop working with the jupyterlab environment. You can use the *logout button*  on the top right of the browser window. As long as the browser window is open and you're connected to the internet you will be logged in. In any other case your session will automatically closed by the server.

If you login again the server will open all the tabs which were open during the logout process. So you can pick up your work at the same place. If you're logged out the server will destroy the session after 30 minutes to give the ressources to the next user! This means that you should logout properly when you don't want to use the system anymore!

------

## 5. FAQ

Here are some questions which may help you in the case that you face some problems with the jupyterlab environment.

- When I logged into the system a see only a white empty page?

  You are probably using a *Microsoft Edge* brower, please use either a *Mozilla Firefox* or Google Chrome/Chromium browser.

- When I logged into the system the webpage is somehow flickering?

  You are probably using an *Apple Safari* browser, please use either a *Mozilla Firefox* or Google Chrome/Chromium browser.

- The jupyterlab environment didn't start normally, what can I do?

  There are different possibilities which prohibit the environment to start. In the past we have faced a few problems:

  - The home directory couldn't be attached to the running session, please inform your tutor or Oliver Cordes !
  - The system is running out of resources, e.g. less CPUs; in this case please be patient and wait a couple of minutes until some of the users logged out!
  - The is a major hardware/software problem, please inform your tutor or Oliver Cordes!

- The contextual help is not working after pressing cmd-/Ctrl-I?

   Probably no conextual help tab is open. Please open a new *Launcher tab* and click on the *Contextual Help* button.



