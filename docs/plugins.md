# Adding Athena plugins
Here are the steps to follow for adding plugins to your Athena project using git:

1. Clone the plugins into a separate directory outside of your Athena project directory.
2. To update the plugins, use git pull in the directory where the plugins are cloned.
3. If you want to make changes to the plugins or create a pull request, create a fork of the plugin repository and clone that instead.
4. Copy and paste the plugin directory into your Athena project folder.
5. Delete the hidden .git folder within the copied directory. Do not delete the .git folder of your Athena project.
6. Check and correct your .gitignore file to ensure that athena-plugin* directories and other necessary files, such as .dll files, are not being ignored.
7. Upload all necessary files to your repository so that you can easily update your server using git pull.

Note: If you direct clone the plugins into your athena project plugin folder: The plugins will be registered as modules and will not be uploaded to your private repository. In GitHub, you will typically see the plugin folder with an arrow symbol, indicating that the source code is not uploaded to your repository. This can be convenient because you can easily update the plugins using git pull, but it may also be inconvenient because you will not be able to update your server in one go or make changes to the plugins.

Removing these folders can be complicated. Try it as follows
1. Remove plugin locally and push your changes to git
2. Look online in git if the plugin folder was removed
3. Copy the plugin back into your local repo. (NOT COPY the .git FOLDER)
4. Push again! Good Luck!
