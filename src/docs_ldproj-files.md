---
layout: docs
permalink: "/docs/application/desktop/ldproj-files/"
title: Live Documenter Project ldproj-files
---
<h1>Live Documenter Project Files</h1>

<p>These files provide a way of managing your documentation outside of single libraries, projects and solutions. 
    Any documentation you have open in Live Documenter can be saved as a project. This allows you to have more 
    control over what libraries are displayed and which are not; further, you can add other solutions, projects 
    and libraries to the documentation as you see fit.</p>

<p>The control provided here will only effect the Live Documenter project file and will not change the solutions,
     projects and libraries in your file system.</p>

## Creating a project file

<p>Project files are created by clicking the save button in Live Documenter, you will then be presented with the 
    normal file dialogue. Once saved the project files can then be opened in the normal manner.</p>

<div class="row justify-content-center p-3">
    <img class="img-fluid image_border" src="/assets/images/documentation/ld-manage-documentation.png" alt="Manage your documentation" />
</div>

<h2>Controlling your documentation</h2>

<p>The + and - icon allow you to control the which libraries from your associated projects and solutions are included in the documentation. Expanding a solution, 
    selecting a library and clicking dont document removes the library from the documentation. Adding new libraries to the documentation include them. Note though
    after modifying the libraries it is important to save the current configuration as a Live Documenter Project. You should then continue to use this project file
    instead of the originating solution or project.</p>

<h3>Removing libraries</h3>

<p>To remove a library you do not want to see in your project click the - symbol and then from the dialogue select 
    the libraries you no longer want active. You can re-activate them later.</p>

<h3>Adding new project and files</h3>

<p>The + button allows you to add new projects, solutions and libraries to the documentation you are viewing. If a 
    solution or Visual Studio project is added the libraries from that are added to the documentation. You can then
     use the remove button to remove unwanted libraries from your project.</p>

<h2>Using projects as a basis for exporting</h2>

<p>After you are happy with the amount of information shown in a project you can use these projects as a basis for 
    export inside the desktop and command line applications.</p>

<p>In the desktop application simply have the project open and click the export button. For the command line application
     you simply need to specify the project where you would normally provide details of the library or Visual Studio 
    project/solution.</p>