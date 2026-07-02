# Day 4 - Package Management Practical

## Objective

Learn how to manage software packages in Ubuntu using APT.

---

## Step 1: Create Lab Directory

```bash
mkdir day4lab
cd day4lab
```

Verify location:

```bash
pwd
```

Output:

```text
/home/rachna/day4lab
```

---

## Step 2: Create Notes File

```bash
touch day4-practical.txt
```

Verify:

```bash
ls
```

Output:

```text
day4-practical.txt
```

---

## Step 3: Update Package Information

```bash
sudo apt update
```

Purpose:

* Refresh package information
* Check available updates
* Download latest package lists

---

## Step 4: Search Package

```bash
apt search tree
```

Purpose:

* Search available packages in repositories

---

## Step 5: Install Package

```bash
sudo apt install tree
```

Purpose:

* Install the tree package

---

## Step 6: Verify Installation

```bash
tree --version
```

Output:

```text
tree v2.3.1
```

Purpose:

* Confirm successful installation

---

## Step 7: Remove Package

```bash
sudo apt remove tree
```

Purpose:

* Remove installed package from the system

---

## Commands Practiced

```bash
sudo apt update
apt search tree
sudo apt install tree
tree --version
sudo apt remove tree
```

---

## Learning Outcome

* Learned Package Management in Linux
* Searched packages using APT
* Installed packages using APT
* Verified package installation
* Removed packages using APT
* Understood package management workflow used on AWS EC2 servers
