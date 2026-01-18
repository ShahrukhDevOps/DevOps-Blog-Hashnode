---
title: "Quoting in Linux"
slug: quoting-in-linux

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
<div data-node-type="callout-text"><strong>Backticks ( ` ) :-</strong> are used for command substitution to execute the command inside them and replace it with the output, but using <code>$()</code> is the modern and preferred alternative.</div>
</div>

### Example:-

```bash
date=`date`
```

### Output :-

```bash
 echo date     
date
```

Here date got substituted as date.