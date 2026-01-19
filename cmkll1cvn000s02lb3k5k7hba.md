---
title: "Quoting in Linux"
seoTitle: "Quoting in Linux Shell Script"
seoDescription: "Learn about quoting in Linux, including single and double quotes, backslashes, backticks, and modern alternatives to handle special characters"
datePublished: Mon Jan 19 2026 19:53:01 GMT+0000 (Coordinated Universal Time)
cuid: cmkll1cvn000s02lb3k5k7hba
slug: quoting-in-linux
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1768851273124/c80569a4-db5d-49ce-975d-c5b70ccc8618.webp
tags: linux, linux-for-beginners, linux-basics, linux-commands, linux-basic

---

Quoting in Linux is a mechanism used in shell scripting and command-line operations to control how special characters (metacharacters) and spaces are interpreted by the shell.

<div data-node-type="callout">
<div data-node-type="callout-emoji">💡</div>
<div data-node-type="callout-text"><strong>Single Quotes (' ')</strong> <strong>:- </strong>Single quotes provide "strong" quoting, meaning everything inside them is treated as a literal string.</div>
</div>

### Example:-

```bash
echo 'What is $LOGNAME'
```

### Output :-

```bash
echo 'What is $LOGNAME'
```

In the output, `$LOGNAME` is not substituted or evaluated; it is printed as is.

<div data-node-type="callout">
<div data-node-type="callout-emoji">💡</div>
<div data-node-type="callout-text"><strong>Double Quotes (" ") :-</strong> Double quotes provide "weak" quoting, which preserves the literal value of most characters but allows for interpretation of certain special characters.</div>
</div>

### Example:-

```bash
variable=world 
echo "hello $variable"
```

### Output:-

```bash
hello world
```

Here, `$variable` is substituted by its value "world".

<div data-node-type="callout">
<div data-node-type="callout-emoji">💡</div>
<div data-node-type="callout-text"><strong>Backslash ( \ )</strong> <strong>:-</strong> The backslash is an escape character that removes the special meaning of the single character immediately following it.</div>
</div>

```bash
echo "This is a backslash: \\"
```

### Output :-

```bash
This is a backslash: \
```

<div data-node-type="callout">
<div data-node-type="callout-emoji">💡</div>
<div data-node-type="callout-text"><strong>Backticks ( ` ) :-</strong> are used for command substitution to execute the command inside them and replace it with the output.</div>
</div>

### Example:-

```bash
sunny=`date`
```

### Output :-

```bash
 echo who is $sunny
who is Tue Jan 20 03:19:09 AM CST 2026
```

Here Sunny got substituted as date.

<div data-node-type="callout">
<div data-node-type="callout-emoji">💡</div>
<div data-node-type="callout-text"><strong>Modern Alternative: </strong><code>$( )</code> :- While backticks work perfectly fine, most modern Linux users prefer using <code>$(command)</code> instead of backticks. It does the exact same thing but is easier to read and allows you to "nest" commands inside each other easily.</div>
</div>

**Example:-**

```bash
now=$(date)
```

### Output :-

```bash
echo Today is $now
Today is Tue Jan 20 03:42:09 AM CST 2026
```

Here now got substituted as date.