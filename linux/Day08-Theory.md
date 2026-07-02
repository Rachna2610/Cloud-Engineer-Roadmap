# Day 8 - Shell Scripting Basics

## What is Shell Scripting?

A Shell Script is a file that contains a series of Linux commands.

Instead of typing commands one by one, we can write them in a script file and execute them together.

Shell scripting helps automate repetitive tasks.

---

## Why Shell Scripting is Important?

Cloud Engineers use shell scripts to:

- Automate server setup
- Install software
- Monitor systems
- Manage backups
- Configure cloud resources

Shell scripting saves time and reduces manual work.

---

## What is Bash?

Bash stands for:

Bourne Again Shell

It is the default shell in most Linux distributions.

Bash interprets and executes commands written in shell scripts.

---

## Shebang (#!)

Every shell script usually starts with:

```bash
#!/bin/bash
```

This line tells Linux to execute the script using Bash.

---

## Creating a Shell Script

Example:

```bash
#!/bin/bash

echo "Hello World"
```

Save as:

```bash
hello.sh
```

Run:

```bash
chmod +x hello.sh
./hello.sh
```

Output:

```text
Hello World
```

---

## Variables

Variables store data.

Example:

```bash
name="Rachna"

echo $name
```

Output:

```text
Rachna
```

---

## User Input

Scripts can accept input from users.

Example:

```bash
echo "Enter your name:"
read name

echo "Hello $name"
```

---

## Using Linux Commands in Scripts

We can execute Linux commands inside scripts.

Example:

```bash
date
pwd
whoami
```

Useful for automation tasks.

---

## Real Cloud Engineer Example

A Cloud Engineer may create a script to:

- Update packages
- Install software
- Create users
- Configure services

instead of running each command manually.

---

## Key Points

- Shell scripts automate tasks.
- Bash is the most common Linux shell.
- Scripts start with #!/bin/bash.
- Variables store values.
- read accepts user input.
- Linux commands can be executed inside scripts.
- Shell scripting is essential for Cloud Engineers.