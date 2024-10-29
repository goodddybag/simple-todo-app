# The step-by-step instructions on how I set up my Jenkins CI/CD pipeline for a Simple Todo application.

### Step 1: Fork this Repository: (https://github.com/sanoojes/simple-todo-app).


### Step 2: Installation of Jenkins on a Windows OS
1. First thing is to install JAVA 21. Link to download JDK: https://phoenixnap.com/kb/install-java-windows 
2. After installing the JDK, then download Jenkins here and install: https://phoenixnap.com/kb/install-jenkins-on-windows 
3. Once installed, I opened `http://localhost:8080` to access Jenkins on my web browser.
   
### Step 3: Create a Jenkins Freestyle Project
1. I clicked on "New Item".
2. I picked "Freestyle project".
3. Named the job "Build Todo App".
   
### Step 4: Configure Source Control
1. On source Code Management:
2. I picked "Git" and enter the URL of the forked repository

### Step 5: Add Build Steps
1. Added an "Execute Windows batch command" build step.
2. In the command box, I added the command to build your app.

```bash
echo "Building HTML/CSS/JS Project"
```
### Step 6: Archive the Build Artifacts
1. For Post-build Actions:
2. I added a post-build action to "Archive the artifacts".
3. Specified the files to archive. 
```plaintext
*.html, *.css, *.js   # This will archive all files in the workspace
```
### Step 7: Save and Verify Build
1. Saved the Job.
2. Clicked on "Build Now" to run the job and build the todo application.
3. After the build completed, I checked the console output for any errors but none.
4. Accessed the archived artifacts from the build's page in Jenkins to see the files generated during the build process.





