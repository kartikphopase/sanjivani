# sanjivani
Batch 1 
Set 1: 
Q 1.  Jira Setup: 
Your team is starting a new project and needs a Jira  Cloud instance to 
track progress. How would you set up a Jira Cloud instance and navigate 
to the project board?
Got it! Here's how you can set up Jira Cloud and access your project board on a Linux system — step by step. Jira Cloud is web-based, so the setup is platform-independent, but I'll include Linux-specific notes (like browser choice, terminal use, etc.) where relevant.

🐧 Step-by-Step Jira Cloud Setup on Linux
✅ 1. Open a Web Browser
On Linux (Ubuntu, Fedora, etc.), you can use any modern browser:

Firefox: firefox &

Chrome: google-chrome & (if installed)

Open Jira's site:

bash
Copy
Edit
xdg-open https://www.atlassian.com/software/jira
✅ 2. Sign Up for Jira Cloud
Click "Get it free" under Jira Software (Cloud version).

Use your email or Google account to sign up.

Choose:

Jira Software

Site name (e.g., myteam.atlassian.net)

Click "Agree and sign up" and wait for the setup.

✅ 3. Create a Project
After login, click “Projects” on the top menu.

Choose "Create project".

Select a template:

Scrum (if you work in sprints)

Kanban (for continuous flow)

Enter:

Project name (e.g., Linux Dev Team)

Key (auto-filled or custom)

Click "Create".

✅ 4. Access the Project Board
From the Projects menu, click your project name.

Select:

“Board” for Kanban

“Backlog” or “Active sprints” for Scrum

You’ll now see your team’s board where you can:

Add issues (tasks, stories, bugs)

Assign team members

Move cards across columns

✅ 5. Add Teammates (Optional)
Go to Project settings (bottom-left menu).

Click “People” > Add people

Enter email addresses and assign roles.

🛠️ Tips for Linux Users
Browser Shortcuts: Use keyboard shortcuts like Ctrl + T (new tab), Ctrl + Shift + T (reopen last closed tab).

Terminal Alias (optional):

bash
Copy
Edit
alias jira='xdg-open https://myteam.atlassian.net'
Want help with setting up boards using curl, REST API, or integrating Jira with Git/Linux workflows? 

Q2 .  Basic Git Operations: 
You’ve updated a project file locally and need to  push the changes to 
GitHub. What Git commands would you use to stage, commit, and push the 
changes? 
To stage, commit, and push your updated file(s) to GitHub, here are the basic Git commands you'd use:

✅ 1. Check the Current Status
bash
Copy
Edit
git status
This shows modified files and lets you confirm what's changed.

✅ 2. Stage the File(s)
To stage a specific file:

bash
Copy
Edit
git add filename.ext
Or to stage all changed files:

bash
Copy
Edit
git add .
✅ 3. Commit the Changes
bash
Copy
Edit
git commit -m "Your commit message here"
Example:

bash
Copy
Edit
git commit -m "Updated main.py with new feature"
✅ 4. Push to GitHub
If you're on the main branch and already have the remote set:

bash
Copy
Edit
git push origin main
If you're working on a different branch:

bash
Copy
Edit
git push origin branch-name
🔁 Quick Summary
bash
Copy
Edit
git status
git add .
git commit -m "Describe your change"
git push origin main

Q3.  JQL Search: 
Your manager asks you to find all Jira issues assigned  to you with the 
status "In Progress." What JQL query would you use to find this 
information? 
To find all Jira issues assigned to you with the status "In Progress", you can use the following JQL (Jira Query Language) query:

jql
Copy
Edit
assignee = currentUser() AND status = "In Progress"
🔍 Explanation:
assignee = currentUser() → Finds issues assigned to you (the logged-in user).

status = "In Progress" → Filters for issues that are currently in progress.

✅ Optional Enhancements:
If you want to sort by due date:

jql
Copy
Edit
assignee = currentUser() AND status = "In Progress" ORDER BY due ASC
To include multiple statuses (e.g., "In Progress" or "In Review"):

jql
Copy
Edit
assignee = currentUser() AND status IN ("In Progress", "In Review")

Set 2: 
Q1.  GitHub Repository: 
You’re collaborating with a colleague on a new project.  How would you 
create a GitHub repository and share it with your teammate? 
To create a GitHub repository and share it with your teammate, follow these simple steps:

✅ 1. Create a New Repository on GitHub
Go to https://github.com and log in.

Click the "+" icon in the top right → select "New repository".

Fill in:

Repository name (e.g., awesome-project)

Description (optional)

Choose Public or Private

Check "Initialize this repository with a README" if you want.

Click "Create repository".

✅ 2. Clone the Repository Locally (Linux-friendly)
Open your terminal and run:

bash
Copy
Edit
git clone https://github.com/your-username/awesome-project.git
cd awesome-project
✅ 3. Add Your Project Files and Push
Add files, then:

bash
Copy
Edit
git add .
git commit -m "Initial commit"
git push origin main
✅ 4. Share the Repository with Your Teammate
Go to your repo page on GitHub.

Click on the “Settings” tab.

Go to “Collaborators” (under “Access”).

Click “Add people”, enter their GitHub username or email, and click Add.

They’ll get an invitation — once accepted, they can clone, push, and pull.


Q 2.  Jira Scrum Project: 
Your team is following the Scrum methodology. How  would you create and 
configure a new Scrum project in Jira? 
To create and configure a new Scrum project in Jira, follow these steps — ideal if your team follows the Scrum methodology with sprints, backlogs, and planning sessions.

✅ 1. Sign In to Jira Cloud
Go to https://www.atlassian.com/software/jira

Sign in with your Atlassian account.

✅ 2. Create a New Scrum Project
From the top menu, click Projects > Create project.

Select the “Scrum” template under "Software Development".

Click Use template.

Enter:

Project Name (e.g., Scrum Dev Team)

Project Key (auto-filled or custom)

Choose Team-managed (simpler setup) or Company-managed (more advanced, customizable workflows).

Click Create project.

✅ 3. Configure Scrum Features
After project creation:

📌 Enable & Use Key Scrum Features:
Backlog View (enabled by default):

Plan stories, bugs, and tasks.

Drag items into sprint and prioritize.

Sprints:

Click “Create Sprint” in the Backlog view.

Add issues to the sprint.

Start the sprint when ready (set sprint goal and duration).

Board View:

Click "Board" in the left sidebar to track progress.

Issues move from To Do → In Progress → Done.

✅ 4. Add Team Members
Go to Project settings > People.

Click Add people and assign roles (e.g., Developer, Admin).

✅ 5. Customize Workflows (Optional)
Go to Project settings > Workflows (for company-managed).

Modify issue statuses or transitions to match your team's Scrum process.

Q3.  Git Branching: 
You want to create a new feature without affecting  the main code. How 
would you create a new branch, switch to it, and merge it back once the 
feature is complete? 
✅ 1. Check Out the Main Branch
Start from the latest version of the main code:

bash
Copy
Edit
git checkout main
git pull origin main
✅ 2. Create a New Branch
Create a branch for your feature (e.g., feature-login):

bash
Copy
Edit
git checkout -b feature-login
This creates and switches to the new branch.

✅ 3. Work on Your Feature
Make changes to your code, then stage and commit:

bash
Copy
Edit
git add .
git commit -m "Added login feature"
You can push your branch to GitHub:

bash
Copy
Edit
git push origin feature-login
✅ 4. Switch Back to the Main Branch
Once your feature is complete and tested:

bash
Copy
Edit
git checkout main
✅ 5. Merge the Feature Branch into Main
bash
Copy
Edit
git merge feature-login
This merges your feature into the main branch.

✅ 6. Push the Updated Main Branch
bash
Copy
Edit
git push origin main
🧹 Optional: Delete the Feature Branch
After merging, you can clean up:

Locally:

bash
Copy
Edit
git branch -d feature-login
On GitHub:

bash
Copy
Edit
git push origin --delete feature-login

Set 3: 
Q1.  Git Installation: 
You’ve set up a new laptop and need to configure  Git with your GitHub 
account. What steps would you take to install Git and link it with your 
GitHub username and email? 
2.  Jira Issue Creation: 
You’ve identified a bug in the project. How would  you create an issue in 
Jira, classify it under the appropriate epic, and assign it to a developer? 
3.  Jira Filter Creation: 
You want to track only high-priority issues in your  project. How would you 
create a JQL filter and save it for future use? 
Set 4: 
1.  Local Git Initialization: 
You’ve just created a new project folder on your  local machine. How would 
you initialize a Git repository and link it to your GitHub repository? 
2.  Git Push and Pull: 
After collaborating with a colleague, you notice  they pushed changes to 
GitHub. How would you pull those updates into your local repository 
without losing your work? 
3.  Jira Dashboard: 
You need to create a dashboard in Jira that shows  open issues, active 
sprints, and completed tasks. How would you achieve this? 
Set 5: 
1.  Jira Navigation: 
Your project lead asks for the sprint backlog and  the active sprint board. 
How would you navigate Jira to find this information? 
2.  Git Commit: 
You’ve made changes to a file but haven’t staged  or committed them. What 
Git commands would you use to add the file and commit the changes with 
a descriptive message? 
3.  Git Merge: 
You’ve completed work on a feature branch and want  to merge it into the 
main  branch. What steps would you follow to ensure  a smooth merge? 
Set 6: 
1.  GitHub Setup: 
You’ve been assigned a new project and need to create  a GitHub 
repository with a  README.md  and a  .gitignore  for .java.  How would you 
achieve this? 
2.  Jira Epic Creation: 
Your team is starting a new initiative that involves  multiple stories and 
tasks. How would you create an epic in Jira and link relevant stories to it? 
3.  JQL Search: 
You need to find all issues in the current sprint  that are still open. What 
JQL query would you use to get this list? 
Set 7: 
1.  Git Commit: 
You’ve made changes to a file but haven’t staged  or committed them. What 
Git commands would you use to add the file and commit the changes with 
a descriptive message? 
2.  Git Pull: 
You’re working on a feature, and your teammate pushed  updates to the 
main  branch. How would you pull those changes into your current branch 
without conflicts? 
3.  Jira Board Configuration: 
Your team prefers a Kanban board for bug tracking.  How would you 
configure a Kanban board in Jira and customize its columns? 
Set 8: 
1.  JQL Search: 
Your manager asks you to find all Jira issues assigned  to you with the 
status "In Progress." What JQL query would you use to find this 
information? 
2.  Jira Story Creation: 
A product owner has described a new feature. How  would you create a Jira 
story with appropriate details and assign it to the development team? 
3.  Git Branching: 
You need to start working on a hotfix while another  feature branch is still 
in progress. How would you create a separate branch for the hotfix and 
merge it into  main  without affecting the other feature branch?
✅ Set 3
Q1. Git Installation & Config (Linux)
bash
Copy
Edit
sudo apt update
sudo apt install git
Configure Git with your GitHub account:

bash
Copy
Edit
git config --global user.name "Your Name"
git config --global user.email "your_email@example.com"
Q2. Jira Bug Issue Creation
Go to your Jira project.

Click “Create” (top menu).

Select Issue Type: Bug

Fill in:

Summary

Description

Select the Epic from the “Epic Link” field.

Set Priority

Assign to developer under Assignee

Click Create.

Q3. Create JQL Filter for High Priority
jql
Copy
Edit
project = "Your Project" AND priority = High
Run the JQL in the search bar.

Click Save As and name your filter (e.g., High Priority Tracker).

Share with team if needed.

✅ Set 4
Q1. Local Git Initialization and Linking
bash
Copy
Edit
cd your_project_folder
git init
git remote add origin https://github.com/your-username/repo-name.git
git add .
git commit -m "Initial commit"
git push -u origin main
Q2. Git Pull without Losing Work
bash
Copy
Edit
git stash
git pull origin main
git stash pop
Q3. Jira Dashboard Creation
Go to Dashboards > Create dashboard

Name it (e.g., Sprint Overview)

Add gadgets:

Filter Results → for open issues

Sprint Health Gadget → for active sprints

Created vs Resolved Gadget → for completed tasks

✅ Set 5
Q1. Jira Navigation for Sprint Info
Go to your project > Backlog → for Sprint Backlog

Click “Active sprints” from the left sidebar to see active sprint board.

Q2. Git Commit (Stage + Message)
bash
Copy
Edit
git add filename.ext
git commit -m "Descriptive message about the change"
Q3. Git Merge (Feature → Main)
bash
Copy
Edit
git checkout main
git pull origin main
git merge feature-branch
git push origin main
✅ Set 6
Q1. GitHub Repo with README and .gitignore
Go to GitHub > New Repository.

Name your repo.

Check:

✔️ Initialize with README.md

✔️ Add .gitignore > Choose Java

Create repo and clone it:

bash
Copy
Edit
git clone https://github.com/your-username/repo-name.git
Q2. Jira Epic Creation & Link Stories
Create a new issue > Choose type Epic.

Fill in epic name, summary, and create.

Create or open stories > set Epic Link to your new epic.

Q3. JQL for Open Issues in Current Sprint
jql
Copy
Edit
sprint in openSprints() AND status != Done
✅ Set 7
Q1. Git Add + Commit
bash
Copy
Edit
git add filename.ext
git commit -m "Added important changes to feature X"
Q2. Git Pull (Safely into Feature Branch)
bash
Copy
Edit
git checkout feature-branch
git pull origin main --rebase
Q3. Jira Kanban Board Setup
Go to Project Settings > Features → Enable Kanban board.

From the board, click Board Settings > Columns

Add or rename columns (e.g., To Do, In Review, Blocked, Done)

✅ Set 8
Q1. JQL for Assigned "In Progress" Issues
jql
Copy
Edit
assignee = currentUser() AND status = "In Progress"
Q2. Create a Jira Story
Click Create

Choose Story as issue type

Add:

Summary

Description (based on product owner’s input)

Components, Priority, Labels

Assign to developer and link to Epic if needed

Click Create

Q3. Git Branch for Hotfix
bash
Copy
Edit
git checkout main
git pull origin main
git checkout -b hotfix-urgent-issue
# After work is done
git add .
git commit -m "Fix critical issue"
git checkout main
git merge hotfix-urgent-issue
git push origin main

Set 9
Jira Cloud Instance – Onboarding & Roles:

Go to Admin > User Management.

Click Invite Users, add email addresses.

Assign project roles under Project Settings > People.

Git Commit and Push:

bash
Copy
Edit
git add .
git commit -m "Updated multiple files"
git push origin main
JQL Query – Bugs in Last 7 Days:

ini
Copy
Edit
labels = Bug AND created >= -7d
Set 10
GitHub Repo with License & Branch Rules:

Create repo via GitHub UI.

Add LICENSE during setup.

Go to Settings > Branches > Add rule.

Set protection for main.

Jira Sprint Creation:

Go to Backlog, click Create Sprint.

Drag items into sprint.

Start it by clicking Start Sprint.

Git Branch Creation and Push:

bash
Copy
Edit
git checkout -b feature-branch
git push origin feature-branch
Set 11
Git Install & Configure on Linux:

bash
Copy
Edit
sudo apt update
sudo apt install git
git config --global user.name "YourName"
git config --global user.email "you@example.com"
Jira Issue Creation – High Priority:

Click Create.

Set type = Bug, Priority = High.

Assign to developer and click Create.

Jira Dashboard Setup:

Go to Dashboards > Create Dashboard.

Add gadgets: Sprint Health, Pie Chart, etc.

Configure each for your board/project.

Set 12
Git Init & Link to GitHub:

bash
Copy
Edit
git init
git remote add origin https://github.com/user/repo.git
git branch -M main
git push -u origin main
Git Pull & Merge Conflict Handling:

bash
Copy
Edit
git pull origin main
# Fix conflicts manually
git add .
git commit -m "Resolved merge conflicts"
Jira Filter – Open Assigned Issues:

JQL:

java
Copy
Edit
status != Done AND assignee = currentUser()
Save as filter and share under "Manage Filters."

Set 13
Jira Scrum Project Setup for Client:

Create project → Select Scrum template.

Go to Project Settings > People, add client with proper role (e.g., Viewer).

Git Add, Commit Specific Files:

bash
Copy
Edit
git add file1.java file2.java
git commit -m "Updated specific files"
git push origin main
Git Merge (No Fast-Forward):

bash
Copy
Edit
git checkout main
git merge --no-ff feature-branch
git push origin main
Set 14
GitHub External Collaboration:

Go to Settings > Collaborators.

Invite by GitHub username or email.

Assign proper access (e.g., Write or Read).

Jira Epic & Story Linking:

Create an Epic.

While creating a story, set Epic Link to that epic.

Delete Git Branch Locally & Remotely:

bash
Copy
Edit
git branch -d feature-branch
git push origin --delete feature-branch
Set 15
Git Update Email:

bash
Copy
Edit
git config --global user.email "newemail@example.com"
Close Sprint & Move Incomplete Tasks:

Go to Active Sprint, click Complete Sprint.

Jira automatically prompts to move unfinished tasks to next sprint or backlog.

JQL Query – Exclude Done Issues:

ini
Copy
Edit
assignee = currentUser() AND status != Done
Set 16
Jira Filter Creation:

Use:

csharp
Copy
Edit
assignee in (membersOf("project-team")) AND status != Done
Save & Share from Filters > Manage Filters.

Jira Kanban Board Setup:

Create a Kanban project.

Go to Board Settings > Columns.

Add/rename columns like To Do, In Progress, QA, Done.

Jira Issue – High Priority:

Click Create → Choose Issue Type (e.g., Bug).

Set Priority = High.

Assign developer and click Create.
