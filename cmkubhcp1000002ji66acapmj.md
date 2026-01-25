---
title: "Variable in Linux"
seoTitle: "Linux Variables & Syntax and Command"
seoDescription: "Learn how to create, access, and manage variables in Linux shell scripting, including user-defined and environment variables, for flexible scripting"
datePublished: Sun Jan 25 2026 22:35:27 GMT+0000 (Coordinated Universal Time)
cuid: cmkubhcp1000002ji66acapmj
slug: variable-in-linux
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1769380345497/f8d76879-e431-40d1-8651-72dc8206ffba.webp
tags: cloud, linux, cloud-computing, devops, linux-for-beginners, linux-basics, linux-commands

---

In Linux shell scripting, a **variable** is essentially a "container" or a named label that stores information (data) in the computer's memory (Ram). You can then use or change that data throughout your script or terminal session by referring to the variable's name.

Here are the key things to know:

### **1\. How to Define a Variable**

To create a variable, you give it a name and assign a value using the `=` sign.  
**Important:** There must be **no spaces** around the `=` sign.

### input:-

```bash
Ganpati=Bappa
```

### **2\. How to Access a Variable**

To use the value stored in a variable, you need to prefix the name with a dollar sign (`$`).

### output will be :-

```bash
echo $Ganpati
Bappa
```

### **3\. Types of Variables**

* **User-defined variables:** Created by you for your own scripts (like the example above).
    

**Environment variables:** Pre-defined variables that store system information. You might have seen some already, like:

* `$USER`: The name of the current user.
    
* `$HOME`: The path to your home directory.
    
* `$PWD`: Your current working directory.
    

### **4\. Why are they useful?**

Variables allow your scripts to be flexible. Instead of "hard-coding" a specific filename or username into your commands, you can use a variable. This way, if the data changes, you only need to update it in one place (where the variable is defined) rather than every time it's used.

<div data-node-type="callout">
<div data-node-type="callout-emoji">💡</div>
<div data-node-type="callout-text"><strong>We can change the value of user defined variable</strong></div>
</div>

### Once the terminal close then changed value of user defined variable get reset and comes to default value.

### 5\. How can we set a value of user-defined variable permanently.

In Linux, when you define a variable in the terminal like `New=York`, It only exists for that specific session. To make it permanent, you need to add it to a shell configuration file. For most Ubuntu users, the default shell is Bash, and the best place to put personal variables is the .bashrc file in your home directory.

### **1\. Open the** `.bashrc` file

You can use `nano`, which is a simple text editor already installed in your environment:

```bash
nano ~/.bashrc
```

### **2\. Add your variable**

Scroll to the very bottom of the file and add your variable using the `export` command. For example:

```bash
export new=york
```

3. Save and Exit Press Ctrl + O then Enter to save.
    
4. Press Ctrl + X to exit the editor.
    
5. Apply the changes
    

The changes will take effect automatically the next time you open a terminal. If you want to use the variable right now in your current session, run:`source ~/.bashrc`

5\. Verify if it works, You can check if your variable is set correctly by typing:

```bash
echo $new
york
```