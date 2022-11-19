---
title: Ubuntu/Debian Development Environment Setup
date: 2022-11-19 16:44:08
tags: ubuntu, debian, development, environment, setup, linux, programming
---

This is a guide to setting up a development environment on Ubuntu/Debian. It is intended to be a quick reference for myself, but it may be useful to others as well.

## Security

### Enable Disk Encryption

If you are using a laptop, you should enable ful disk encryption. The full disk encryption need to happen at install time. I'm running on PopOs and it gives the option of enabling full disk encryption during the install process, I am not sure about other distros.

### System updates

The first thing you should do is update the system and install security updates. This can be done with the following commands:

```bash
sudo apt update
sudo apt upgrade
sudo apt dist-upgrade
```

## Installing Desktop Applications

Your OS comes with an app store which has most app but it might sometimes lack some of the apps you need so instead you can use flatpack.

[Flatpack](https://flatpak.org/) is the new standard for Desktop applications on Linux. It is a sandboxed application.

To install flatpack run the following command:

```bash
sudo apt install flatpak
```

To install an application run the following command:

```bash
flatpak install flathub <app-name>
```

Some of the apps I use are: Whatsapp, Discord, Slack, Postman, chrome, calibre, Trilium, VLC Media Player, Zoom, and Discord.

## Installing Development Tools

Don't install IDE and other development tools from the app store or flatpack. Instead, install them from the terminal. This will make it easier to update them.

Install the build-essential package.

```bash
sudo apt install build-essential
```

### Visual Studio Code

Visual Studio Code is a powerful desktop editor for programming, with built-in support for version control and debugging. The large range of extensions for Visual Studio Code enable it to work with every popular programming language and framework. It is available free of charge, [Get it here](https://code.visualstudio.com/).

### Jetbrains IDEs

Personally I think Jetbrains IDEs are the best IDEs for programming they have higher intellisense . They are available for free for students and teachers. [Get it here](https://www.jetbrains.com/student/).

### Lapce

Lapce is a lightweight code editor for programming built in Rust. It is available for free, [Get it here](https://lapce.dev/)

### Text Editors

Ubuntu comes with a text editor called Gedit. It is a simple text editor that is good for editing text files. It becomes handy when you pair it with the terminal. To open a file in Gedit from the terminal run the following command:

```bash
gedit <file-name>
```

## Installing Programming Languages

Ubuntu comes with C, C++, and Python pre-installed.

### Node.js

To install Node.js, we will use nvm (Node Version Manager). Nvm is a tool that allows you to install and manage multiple versions of Node.js.
To install nvm run the following command:

```bash
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.38.0/install.sh | bash
```

To install the LTS version of Node.js run the following command:

```bash
nvm install --lts
```

### Go

To install Go, run the following command:

```bash
sudo apt install golang
```

## Installing Databases

You should consider using containers for databases. Containers are isolated environments that run on top of your OS. They are lightweight and easy to setup. They are also easy to backup and restore and also enable you to have multiple versions of the database server.

### PostgreSQL

To install PostgreSQL, run the following command:

```bash
sudo apt install postgresql
sudo postgresql-setup --initdb
sudo systemctl enable postgresql
sudo systemctl start postgresql
```

```
Work In Progress
```
