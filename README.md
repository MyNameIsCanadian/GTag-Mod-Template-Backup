# GTag-Mod-Template-Backup
https://www.youtube.com/watch?v=tNeaQwqWxF4
# [QPM] Quest Package Manger
https://github.com/sc2ad/QuestPackageManager/actions/runs/1655161985
# How to BSaber Quest Modding Guide
We will start from Lauriethefish's project template. It's made to use the VSCode Project Templates extension by cantonios. If you're using VSCode and the extension, see the next section (Using VSCode Project Templates), otherwise skip to the one after (Without Project Templates)

Using VSCode Project Templates
With the VSCode extension installed:

Open the project templates folder (Ctrl+Shift+P > Project: Open Templates Folder) and extract the Quest mod template into a new folder inside the templates folder.
Create a new empty folder for your project somewhere and open it in VSCode (File > Open Folder...)
Create a project from the template (Ctrl+Shift+P > Project: Create Project from Template)
For ndkpath, add the path to your NDK using forward slashes.
id is the internal name of your mod (no spaces).
name is the readable name of your mod.
author is your name or handle.
description is a short description of your mod.
Without Project Templates
Extract the template ZIP into a new folder somewhere.
For each .ps1 file, right click > Properties > Check "Unblock" on the lower right. This will prevent a security confirmation every time you run one of the scripts.
Find and replace each of the project template tags throughout the project:
Replace #{ndkpath} with the path to your NDK using forward slashes.
Replace #{id} with the internal name of your mod (no spaces).
Replace #{name} with the readable name of your mod.
Replace #{author} with your name or handle.
Replace #{description} with a short description of your mod.
In case the template may be updated with additional tags, you may want to do an extra project wide search for the template tag format (e.g. #\{([^}]+)\} if you have regex search)
Once your project directory is set up and all template tags have been replaced.

Run qpm restore. This will download the dependencies defined in qpm.json. When you add or change a dependency, rerun the command. See the qpm repository for more information on using qpm.
To run an initial test build, run build.ps1.
Tips and tricks:

Commands can be run from a PowerShell terminal inside VSCode (Terminal > New Terminal or Ctrl+Shift+`)
