# Day 9 - Advanced Shell Scripting

## Introduction

Advanced Shell Scripting allows scripts to make decisions, repeat tasks, and organize code efficiently.

These concepts are used heavily in Linux administration and cloud automation.

---

## Conditional Statements

Conditional statements allow scripts to make decisions.

Example:

```bash
if [ $num -gt 10 ]
then
    echo "Greater than 10"
else
    echo "10 or less"
fi
```

The script performs different actions based on conditions.

---

## Comparison Operators

| Operator | Meaning |
|-----------|-----------|
| -eq | Equal |
| -ne | Not Equal |
| -gt | Greater Than |
| -lt | Less Than |
| -ge | Greater Than or Equal |
| -le | Less Than or Equal |

Example:

```bash
if [ $age -ge 18 ]
```

---

## For Loop

A for loop repeats a task multiple times.

Example:

```bash
for i in 1 2 3 4 5
do
    echo $i
done
```

Output:

```text
1
2
3
4
5
```

---

## While Loop

A while loop runs while a condition is true.

Example:

```bash
count=1

while [ $count -le 5 ]
do
    echo $count
    count=$((count+1))
done
```

---

## Functions

Functions help reuse code.

Example:

```bash
greet() {
    echo "Welcome"
}

greet
```

Output:

```text
Welcome
```

Benefits:

- Reusability
- Cleaner scripts
- Easier maintenance

---

## Exit Status

Every Linux command returns an exit status.

```bash
echo $?
```

Meaning:

| Value | Meaning |
|---------|----------|
| 0 | Success |
| Non-Zero | Error |

Example:

```bash
ls
echo $?
```

---

## Debugging Shell Scripts

Debugging helps identify problems.

Run:

```bash
bash -x script.sh
```

Linux shows each command before execution.

Useful for troubleshooting automation scripts.

---

## Real Cloud Engineer Example

Cloud Engineers use advanced shell scripts for:

- Server deployment
- Backup automation
- Log cleanup
- Monitoring tasks
- EC2 instance configuration

---

## Key Points

- if-else statements make decisions.
- Loops repeat tasks automatically.
- Functions improve code reusability.
- Exit status indicates success or failure.
- bash -x helps debug scripts.
- Advanced shell scripting is widely used in cloud automation.