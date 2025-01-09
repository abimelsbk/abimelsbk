---
title: "Print Your Names ( Git & GitHub Project )"
datePublished: Tue Sep 19 2023 18:23:57 GMT+0000 (Coordinated Universal Time)
cuid: clmqn96oe000309mv48zxdynd
slug: print-your-names-git-github-project

---

### **Clone the Repository Locally**

```bash
git clone <repository_url>
```

Each student needs to clone the repository to their local machine using the following command. They should replace `<repository_url>` with the URL of the project GitHub repository

Repo Link : [Print Your Name](https://github.com/abimelsbk/Print-your-name.git)

### **Create a New Branch**

Students create a new branch in their local repository to work on their individual contributions. This branch can have a descriptive name related to the specific task they are working on. Here it can be your name itself ( NB: don't include space in the branch name )

```xml
git checkout -b branch_name
```

Insert your branch name in the above command. The above command creates a new branch as your name and Switch from the master to the newly created branch

### **Edit the HTML File**

In the cloned repository, students can locate the HTML file ( `index.html` ) with the following content:

```xml
<!DOCTYPE html>
<html>
<head>
    <title>Student Names</title>
</head>
<body>
    <h1>Student Names</h1>
    <!-- Students should add their names here -->
</body>
</html>
```

Each student should insert their name into the HTML file within the `<h1>` tag, like this:

```xml
<h1>John Doe</h1>
```

Save the file after adding their name.

### **Commit and Push Changes**

Next, students should commit their changes and push them to the GitHub repository. Here are the commands:

```bash
# Add the changes to the staging area
git add index.html

# Commit the changes with a descriptive message
git commit -m "Add [Student Name]'s name"

# Push the changes to the GitHub repository
git push origin your_branch_name
```

Replace `your_branch_name` with yours

### **Create a Pull Request**

1. After pushing their changes, students can go to the GitHub repository's page.
    
2. Click the "Pull Requests" tab and then click the "New Pull Request" button.
    
3. In the base repository section, ensure the base branch is set to the default branch (e.g., `master`).
    
4. In the "compare" branch section, select the branch you created and worked on.
    
5. Click the "Create Pull Request" button.
    

---

### For Queries Contact

[Abimel S B kulumala](https://www.linkedin.com/in/abimelsbkulumala/)